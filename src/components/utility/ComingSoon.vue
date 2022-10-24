<template>

  <main class="fixed top-0 left-0 bottom-0 right-0 flex items-center px-4 md:px-16 lg:px-20">

    <article class="">
      <a href="https://onegoodcard.me/profile/jacobcarter" target="_blank" class="hidden md:block">

        <div class="flex items-center">

        <div class="w-24 rounded-full aspect-square" style="background-image: url('/assets/images/photos/jacobcarterheadshot.png')">

        </div>
        <div class="ml-4">
          <strong class="text-white m-0 font-size-22">
            Jacob J. Carter
          </strong>
          <p class="text-white m-0 font-size-20">
            Web Developer
          </p>
        </div>

        </div>

      </a>
      <h2 class="text-white font-size-84 lg:w-2/3 md:mt-8">
        Our website is coming soon!
      </h2>

      <p class="text-white font-size-20 md:w-2/3 lg:w-1/2 mt-2 md:mt-8">
        Thank you for being patient. We’re doing some work on the website, so feel free to check back in later. If you have any inquiries please don’t hesitate to contact me through my details below:
      </p>

      <div class="mt-2 md:mt-8">
        <div class="flex items-center">
          <svg xmlns="http://www.w3.org/2000/svg" width="1.5em" height="1.5em" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24"><path fill="white" d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5l-8-5V6l8 5l8-5v2z"/></svg>
          <a href="mailto:jacob@choicedigital.studio" class="text-white font-size-20 underline ml-4">
            jacob@choicedigital.studio
          </a>
        </div>
        <div class="flex items-center mt-2">
          <svg xmlns="http://www.w3.org/2000/svg" width="1.5em" height="1.5em" preserveAspectRatio="xMidYMid meet" viewBox="0 0 1200 1200"><path fill="white" d="M600 0C268.629 0 0 268.629 0 600s268.629 600 600 600s600-268.629 600-600S931.371 0 600 0zM384.375 238.33c12.362-.729 23.536 6.66 32.007 19.775l82.031 155.566c8.637 18.434 3.729 38.172-9.155 51.343l-37.573 37.573c-2.319 3.178-3.845 6.757-3.882 10.693c14.409 55.775 58.117 107.223 96.681 142.603c38.562 35.38 80.009 83.281 133.812 94.629c6.65 1.855 14.797 2.52 19.556-1.903l43.652-44.458c15.068-11.421 36.866-16.956 52.954-7.617h.732l148.021 87.378c21.728 13.619 23.979 39.944 8.423 55.957L849.683 941.016c-15.056 15.44-35.058 20.631-54.491 20.654c-85.948-2.575-167.158-44.759-233.862-88.11c-109.49-79.653-209.923-178.446-272.975-297.803c-24.182-50.05-52.589-113.91-49.878-169.774c.242-21.016 5.928-41.605 20.728-55.151l101.953-101.953c7.942-6.758 15.799-10.111 23.217-10.549z"/></svg>
          <p class="text-white font-size-20 ml-4">
            +44 7963 311156
          </p>
        </div>
        

      </div>

    </article>

  </main>

</template>


<script lang="ts">
import { Icon } from '@iconify/vue';

export default {
  name: 'ComingSoon',
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

  main {
    z-index: 9999;
    max-height: 100vh;

    background-color: #0E0E0E;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='100%25' height='100%25'%3E%3Cdefs%3E%3Cpattern id='p' width='100' height='100' patternUnits='userSpaceOnUse'%3E%3Cpath id='a' data-color='outline' fill='none' stroke='%23181818' stroke-width='15' d='M50 47.5v5M52.5 50h-5'%3E%3C/path%3E%3C/pattern%3E%3C/defs%3E%3Crect fill='url(%23p)' width='100%25' height='100%25'%3E%3C/rect%3E%3C/svg%3E");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;



    
  }
  article {
    max-width: 110em;
    margin:0 auto;
  }

  h2 {
    font-family: 'Felix', 'Montserrat' ,sans-serif;
    max-width: 10em;
    font-weight: normal;
  }

  strong, p, a {
    font-family: 'Montserrat', sans-serif;
    max-width: 95ch;
  }

</style>