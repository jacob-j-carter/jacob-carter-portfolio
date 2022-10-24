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
    transition: translate 150ms linear;

    
    background-color: #FFFFFF;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink' width='100%25' height='100%25'%3E%3Cdefs%3E%3Cpattern id='p' width='150' height='90' patternUnits='userSpaceOnUse'%3E%3Cpath id='a' data-color='outline' fill='none' stroke='%23F6F6F6' stroke-width='5' miterlimit='10' d='M75 0H25L0 45l25 45h50l25-45L75 0zM41.4546 80.127L50 64.7462l-5.4849-9.8732H33.5455L25 70.255 10.9697 45 25 19.745l8.5455 15.3819h10.9697l5.4861-9.871L41.4546 9.873h28.0605l14.0303 25.254H66.4549L60.9697 45l5.4851 9.873h17.0905L69.5151 80.127H41.4546zM75.0001 19.7458l-5.485-9.8728H58.5455L44.5151 35.127H16.4546L10.9697 45l5.4849 9.873h28.0605l14.0304 25.254h10.9696l5.485-9.8728L60.9697 45zM50.0012 45H10.9697M69.5151 9.873L50.0012 45M69.5151 80.127L50.0012 45M44.5151 54.873L25 90M100 45H60.9697M25 0l19.5151 35.127'%3E%3C/path%3E%3Cuse xlink:href='%23a' x='-75' y='-45'%3E%3C/use%3E%3Cuse xlink:href='%23a' x='-75' y='45'%3E%3C/use%3E%3Cuse xlink:href='%23a' x='75' y='-45'%3E%3C/use%3E%3Cuse xlink:href='%23a' x='75' y='45'%3E%3C/use%3E%3C/pattern%3E%3C/defs%3E%3Crect fill='url(%23p)' width='100%25' height='100%25'%3E%3C/rect%3E%3C/svg%3E");
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
    animation: darken 150ms linear;
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
