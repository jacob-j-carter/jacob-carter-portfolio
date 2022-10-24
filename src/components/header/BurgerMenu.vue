<template>
  <div :class="[navHidden ? '' : 'overlay-on']" >
    <nav
      class="bg-stone-600 w-2/3 md:w-2/5 right-0 flex flex-col items-center justify-center fixed z-30"
      :class="[navHidden ? 'nav-hidden' : '']"
    >
      <div @click="$emit('close-nav')">
        <Icon icon="ei:close" width="32" class="text-black absolute right-4 top-4 w-8 h-8" />
      </div>

      <div :key="page.pageName" v-for="page in pages" class="my-8">
        <a :href="page.pageHREF" @click="$emit('close-nav')">
          <h3 class="uppercase text-black" :class="[pageName == page.pageName ? 'heading-font' : 'button-font']">
            {{ page.pageName }}
          </h3>
        </a>
      </div>
    </nav>
  </div>
</template>

<script lang="ts">
import pageData from "../../data/pageData.json";
import Button from "../interactive/Button.vue";
import { Icon } from '@iconify/vue';


export default {
  name: "BurgerMenu",
  components: {
    Button,
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

    
        
    background-color: #F6F6F6;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink' width='100%25' height='100%25'%3E%3Cdefs  data-stroke-max-alt='48'%3E%3Cpattern id='p' width='100' height='100' patternUnits='userSpaceOnUse'%3E%3Cpath id='a' data-color='fill' fill='%23FFFFFF' d='M0 0h50v50H0zM50 50h50v50H50zM35.355 50h-20.71L0 64.645v20.71L14.645 100h20.71L50 85.355v-20.71zM85.355 0h-20.71L50 14.645v20.71L64.645 50h20.71L100 35.355v-20.71z'%3E%3C/path%3E%3C/pattern%3E%3C/defs%3E%3Crect fill='url(%23p)' width='100%25' height='100%25'%3E%3C/rect%3E%3C/svg%3E");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;


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
