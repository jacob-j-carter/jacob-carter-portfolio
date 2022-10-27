<template>

  <PortfolioTemplate :projectIndex="1" />

</template>


<script lang="ts">
import { Icon } from '@iconify/vue';
import PortfolioTemplate from './PortfolioTemplate.vue';

export default {
  name: 'CSSDisplayInfo',
  components: {
		Icon,
    PortfolioTemplate,
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