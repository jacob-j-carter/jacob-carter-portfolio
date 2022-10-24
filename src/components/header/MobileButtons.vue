<template>

  <header class="flex justify-between items-center w-full p-4 mx-auto absolute z-10">

  <a href="/">
    <h2 class="md:hidden text-white font-size-96 header-logo">C</h2>
    <h2 class="hidden md:flex uppercase text-white font-size-96 header-logo">Carter</h2>
  </a>

  <div class="" @click="$emit('toggle-menu')">

    <img src="/assets/images/icons/burgermenu.svg" alt="open menu icon">

  </div>

  </header>

</template>


<script lang="ts">
import { Icon } from '@iconify/vue';

export default {
  name: 'MobileButtons',
  components: {
		Icon,
	},
  // props: {

  // },
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

  .header-logo {
    font-family: 'FogTwoNo5', sans-serif;
  }

</style>