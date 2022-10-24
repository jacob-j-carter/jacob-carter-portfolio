<template>

  <section class="mt-40">
		
    <article class="wrapper px-4">
      <h1 class="text-white">
        <span id="header_jacob-carter">jacob carter </span>
        <span>is a </span>
        <span class="header-portion">digital developer </span>
        <span>& </span>
        <span class="header-portion">lover of coffee</span>
      </h1>
      <h2 class="sr-only">
        jacob carter is a digital developer and lover of coffee
      </h2>

      <a href="mailto:jacob@choicedigital.studio">
        <button class="flex mt-20 font-size-28">
          Say Hello
          <div class="w-6 ml-4">
            <img src="/assets/images/icons/handwave.svg" alt="hand waving icon" class="w-full" />
          </div>
        </button>
      </a>

    </article>

	</section>

</template>


<script lang="ts">
import { Icon } from '@iconify/vue';

export default {
  name: 'Hero',
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

  h1 > span {
    opacity: .3;
  }

  h1:hover > .header-portion:hover {
    opacity: 1;
    cursor:pointer;
  }


  #header_jacob-carter {
    opacity: 1;
  }

</style>