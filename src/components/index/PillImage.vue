<template>

  <img :src="'/assets/images/photos/pill-' + imgName + '.png'" :alt="imgAlt" class="inline mx-2 h-8">

</template>


<script lang="ts">
import { Icon } from '@iconify/vue';

export default {
  name: 'PillImage',
  components: {
		Icon,
	},
  props: {
    imgName: String,
    imgAlt: String
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