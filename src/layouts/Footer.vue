<template>
  <footer class="mt-36 w-full flex flex-col items-center p-4 relative">

    <a href="mailto:jcarterfreelance@outlook.com">
      <button class="heading-font font-size-56 items-center flex justify-center px-16 py-16 mb-36">
        Say hello
      </button>
    </a>

    <!-- Footer Text -->
    <div class="md:flex md:justify-between w-full">
      <div class="text-white w-full">
        <p class="text-right md:text-left"><span>&#169;</span>{{new Date().getFullYear()}}</p>
        <p class="uppercase text-right hidden md:inline md:text-left">All Rights Reserved</p>
      </div>
      <div class="text-white">
        <p class="text-right"><a href="mailto:jcarterfreelance@outlook.com">jcarterfreelance@outlook.com</a></p>
      </div>
    </div>

    <div class="blur-container-2 flex justify-between items-center">
      <div class="yellow-blur"></div>
      <div class="yellow-blur"></div>
		</div>

  </footer>
</template>


<script lang="ts">
import { Icon } from '@iconify/vue';

export default {
  name: 'Footer',
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
  @use '../sass/abstracts' as *;
  @use '../sass/themes' as *;

  button {
    border: 1px solid white;
    rotate: -5deg;
    background: none;

    &:hover {
      background-color: white;
      color: black;
    }
  }

  .blur-container-2 {
  height: 10em;
  width: 40em;
  bottom:14em;
  z-index: -1;
  animation: blurSpin 20000ms linear infinite;
  position: absolute;

  .yellow-blur {
    background: radial-gradient(50% 50% at 50% 50%, #F7B801 0%, rgba(247, 184, 1, 0) 100%);
    opacity: 0.5;
    filter: blur(25px);
    aspect-ratio: 1;
    width: 10em;
  }

  @keyframes blurSpin {
    0% {
      rotate: 0deg;
    }
    100% {
      rotate: 360deg;
    }
  }
  }

</style>