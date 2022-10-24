<template>

  <header class="flex justify-between items-center w-full p-2 mx-auto absolute z-10">

  <div class="w-16 h-16 bg-stone-500 rounded-xl p-2">
    <a href="/">
      <Icon icon="carbon:logo-vue" width="100%" class="text-white" />
    </a>
  </div>

  <div class="w-16 h-16 bg-stone-500 rounded-xl p-2" @click="$emit('toggle-menu')">

    <Icon icon="cil:hamburger-menu" width="100%" class="text-white" />
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



</style>