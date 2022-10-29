<template>
  <div :class="[navHidden ? '' : 'overlay-on']" >
    <nav
      class="bg-black w-2/3 md:w-2/5 right-0 flex flex-col items-center justify-center fixed z-30"
      :class="[navHidden ? 'nav-hidden' : '']"
    >
      <div @click="$emit('close-nav')">
        <Icon icon="ei:close" width="32" class="text-white absolute right-4 top-4 w-8 h-8" />
      </div>

      <div :key="page.pageName" v-for="page in pages" class="my-8">
        <a :href="page.pageHREF" @click="$emit('close-nav')">
          <h3 class="uppercase text-white" :class="[pageName == page.pageName ? 'line-through' : 'button-font font-size-40']">
            {{ page.pageName }}
          </h3>
        </a>
      </div>
      <div class="flex items-start relative top-24">
        <a href="https://github.com/Choice-Studio" target="_blank">
          <Icon icon="akar-icons:github-fill" class="text-white hover:text-stone-400 text-lg mr-4" />
        </a>
        <a href="https://www.linkedin.com/in/jacob-j-carter/" target="_blank">
          <Icon icon="akar-icons:linkedin-box-fill" class="text-white ml-4 hover:text-stone-400 text-lg" />
        </a>
      </div>
    </nav>
  </div>
</template>

<script lang="ts">
import pageData from "../../data/pageData.json";
import { Icon } from '@iconify/vue';


export default {
  name: "BurgerMenu",
  components: {
    Icon
},
  props: {
    pageName: {
      type: String
    },
    navHidden: {
      type: Boolean
    }
  },
  data () {
    return {
      pages: pageData,
    };
  },
  methods: {

  },
  created() {
    
  },
};
</script>

<style scoped lang="scss">
  @use '../../sass/abstracts' as *;
  @use '../../sass/themes' as *;

  nav {
    height: 100vh;
    transition: translate 200ms linear;



  }

  .nav-hidden {
    translate: 100% 0;
  }

  .overlay-on::after {
    content:"";
    display: block;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: 20;
    background-color: black;
    animation: darken 200ms linear;
    opacity: .75;

    @keyframes darken {
      0% {
        opacity: 0;
      }
      100% {
        opacity: .75;
      }
    }
  }

</style>
