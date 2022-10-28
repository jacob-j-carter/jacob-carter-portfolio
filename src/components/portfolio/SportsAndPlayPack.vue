<template>

  <article class="px-4 md:px-16 wrapper">
    <PortfolioTemplate :projectIndex="1" />

    
    <section class="my-8">
      <h2 class="text-white font-size-48 my-8 md:mt-16">
        Goal of project
      </h2>
      
      <p class="text-white md:w-2/3">
        Sports & Play Consulting Ltd. is a small consulting firm in South West England which specializes in giving specialist advice to government bodies, such as schools and parish councils, relating to construction projects, safety regulations, and others services.
        <br>
        <br>
        Being physically limited to areas in proximity to the Gloucestershire area, Sports & Play Consulting Ltd. looked to expand its reach through a remote consulting service for schools starting new construction projects.
        <br>
        <br>
        My task for this project was to create a professional website for hundreds of schools to view across the UK. Sports & Play Consulting Ltd. needed a way for schools to purchase a ‘pack’ that would include a zip file including a set of instructions and advice that schools would use in their project.
        <br>
        <br>
        For this requirement, I choice WordPress, Avada Theme, and Woo Commerce. Of course, Figma was used for the UI/UX design.
      </p>
      
      <h2 class="text-white font-size-48 my-8 md:mt-16 lg:mt-20">
        Challenges Faced
      </h2>
      
      <p class="text-white md:w-2/3">
        More than any previous client project, I managed to design a wireframe and hi-fi Figma prototype that was almost identical to the final product. Being a relatively simple project, there weren’t many technical hiccoughs. However, my problems came about when trying to deploy the website.
        <br>
        <br>
        Without the knowledge I have now of front-end website deployment services, such as Netlify and Vercel, my only obvious option at the time was to create a custom WordPress theme for CSS Display Info. Creating a WordPress theme took an unnecessary amount of time to learn and develop, though it gave me some beginner knowledge into PHP.
        <br>
        <br>
        This was also my first encounter with browser support issues. I learnt after publishing the website, through a comment on Reddit, that the websites UI had been terribly disfigured on Mozilla Firefox. I later found out that some of the methods of importing fonts, animations, and the blur property had differing levels of support to other browsers, such as Chrome and Opera. I later fixed these discrepancies when I moved from WordPress to Netlify.
      </p>
    </section>

    <section class="md:mt-16 md:grid md:grid-cols-2">
      <div class="md:mr-2">
        <h2 class="text-white font-size-48 my-8">
          Wireframes  
        </h2>
        <img :src="'/assets/images/portfolio/sportsandplaypack/showcase/wireframe/package.png'" :alt="'Wireframe of ' + projectName + ' website'" class="w-full">
      </div>
    
      <div class="md:ml-2">
        <h2 class="text-white font-size-48 my-8">
          Final Product
        </h2>
        <img :src="'/assets/images/portfolio/sportsandplaypack/showcase/final/package.png'" :alt="'Screenshot of ' + projectName + ' website'" class="w-full">
      </div>
    </section>

    <div class="flex justify-end w-full mt-8 md:mt-16">
      <a :href="project.websiteURL" target="_blank">
        <button class="flex font-size-24 items-center mt-8 md:mt-0">
          View Live Site
          <div class="w-6 ml-4">
            <img src="/assets/images/icons/arrow.svg" alt="hand waving icon" class="w-full" />
          </div>
        </button>
      </a>
    </div>

  </article>
  
  

</template>


<script lang="ts">
import { Icon } from '@iconify/vue';
import PortfolioTemplate from './PortfolioTemplate.vue';
import portfolioItems from '../../data/portfolioItems.json'

export default {
  name: 'CSSDisplayInfo',
  components: {
		Icon,
    PortfolioTemplate,
	},
  // props: {

  // },
  data () {
    return {
      project: portfolioItems[1],
      projectName: 'Sports & Play Pack',
      projectLink: 'sportsandplaypack',
    }
  },
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