<template>

  <section class="mt-40 md:mt-56 md:mb-48 lg:mt-40 relative">

    

    <article class="wrapper px-4 md:px-16 lg:px-0">
      <h1 class="text-stone-200 pt-4 mb-24 lg:w-4/5 relative">
        <span id="header_jacob-carter">jacob carter </span>
        <span>is a </span>
        <span id="digital-developer" class="header-portion" @mousemove="updateCoordinates" >digital developer </span>

        <img src="https://media3.giphy.com/media/3oKIPnAiaMCws8nOsE/giphy.gif?cid=ecf05e47sxnh5ksz4i0y3koysrsw6fr7k7qs3v15p2fwqudc&rid=giphy.gif&ct=g" alt="" :style="'top:' + (y * .4) + 'px;' + 'left:' + (x * .5) + 'px;'" id="cursor-developer" class="gif-cursor">

        <span>& </span>
        <span class="header-portion" @mousemove="updateCoordinates" id="lover-of-coffee">lover of coffee</span>

        <img src="https://media0.giphy.com/media/Y0jN3XvfZCNWM/giphy.gif?cid=ecf05e472izy4ye97vsyat4d52ucwqisvhkfnjhffcb2mwh9&rid=giphy.gif&ct=g" alt="" :style="'top:' + (y * .5) + 'px;' + 'left:' + (x * .55) + 'px;'" id="cursor-coffee" class="gif-cursor">

      </h1>
      <h2 class="sr-only">
        jacob carter is a digital developer and lover of coffee
      </h2>

      <div class="md:flex items-end">
        <a href="#library" class="hidden md:inline">
          <button class="flex font-size-24 items-center md:mr-12">
            My Projects
            <div class="w-6 ml-4">
              <img src="/assets/images/icons/briefcase.svg" alt="briefcase icon" class="w-full" />
            </div>
          </button>
        </a>
        <a href="mailto:jacob.young.carter@gmail.com">
          <button class="flex font-size-24 items-center">
            Say Hello
            <div class="w-6 ml-4">
              <img src="/assets/images/icons/handwave.svg" alt="hand waving icon" class="w-full" />
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
  data() {
    return {
      x: 500,
      y: 350,
      cursorOpacity: 0
    }
  },
  methods: {
    updateCoordinates: function(event) {
      this.x = event.clientX;
      this.y = event.clientY;
    },
  }
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

  .gif-cursor {
    position: absolute;
    width: 3em;
    border-radius: .5em;
    translate: -50% -50%;
    transition: top 500ms linear, left 500ms linear, opacity 150ms linear;
    opacity: 0;
    z-index: -1;
  }


  @media only screen and (min-width: 1024px) {
    // ==== For Desktop Screens Only ====   
      h1:hover > .header-portion:hover {
        opacity: 1;
      }

      #digital-developer:hover ~ #cursor-developer {
        opacity: 1;
      }
      #lover-of-coffee:hover ~ #cursor-coffee {
        opacity: 1;
      }
}

</style>