<template>
  <div class="hidden lg:flex">

    <header class="w-full h-16 flex items-center justify-between px-8">

      <a href="/">
        <h2 class="hidden md:flex uppercase text-white font-size-36 header-logo">Carter</h2>
      </a>

      <div class="flex">
        <div class="flex items-center justify-end text-white">
          <a :key="page.pageName" v-for="page in pages" :href="page.pageHREF" class="button-font font-size-14 mx-6 hover:opacity-70" :class="[pageName == page.pageName ? 'line-through' : '']">{{ page.pageName }}</a>
        </div>
        <div class="flex items-start">
          <a href="https://github.com/Choice-Studio" target="_blank">
            <Icon icon="akar-icons:github-fill" class="text-white hover:text-stone-400" />
          </a>
          <a href="https://github.com/Choice-Studio" target="_blank">
            <Icon icon="akar-icons:linkedin-box-fill" class="text-white ml-4 hover:text-stone-400" />
          </a>
        </div>
      </div>

    </header>

  </div>
</template>


<script lang="ts">
import pageData from '../../data/pageData.json';
import { Icon } from '@iconify/vue';

export default {
  name: 'DesktopHeader',
  props: {
    pageName: String
  },
  data () {
    return {
      pages: pageData,
    };
  },
  components: {
		Icon,
	},
  // data () {
  //   return {
      
  //   }
  // },
  // methods: {

  // },
  // created () {

  // }
}

</script>


<style scoped lang="scss">
  @use '../../sass/abstracts' as *;
  @use '../../sass/themes' as *;


</style>