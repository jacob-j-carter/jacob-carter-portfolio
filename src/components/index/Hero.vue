<template>

  <section class="mt-40 md:mt-56 md:mb-48">
		
    <article class="wrapper px-4 md:px-16">
      <h1 class="text-stone-200 pt-4 mb-24">
        <span id="header_jacob-carter">jacob carter </span>
        <span>is a </span>
        <span class="header-portion">digital developer </span>
        <span>& </span>
        <span class="header-portion">lover of coffee</span>
      </h1>
      <h2 class="sr-only">
        jacob carter is a digital developer and lover of coffee
      </h2>

      <div class="md:flex items-end">
        <a href="mailto:jacob@choicedigital.studio">
          <button class="flex font-size-28 items-center">
            Say Hello
            <div class="w-6 ml-4">
              <img src="/assets/images/icons/handwave.svg" alt="hand waving icon" class="w-full" />
            </div>
          </button>
        </a>
        <a href="#library" class="hidden md:inline">
          <button class="flex font-size-28 items-center md:ml-12">
            My Projects
            <div class="w-6 ml-4">
              <img src="/assets/images/icons/briefcase.svg" alt="briefcase icon" class="w-full" />
            </div>
          </button>
        </a>
      </div>

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


  #header_jacob-carter {
    opacity: 1;
  }


  @media only screen and (min-width: 1024px) {
    // ==== For Desktop Screens Only ====   
      h1:hover > .header-portion:hover {
        opacity: 1;
        cursor:pointer;
      }
}

</style>