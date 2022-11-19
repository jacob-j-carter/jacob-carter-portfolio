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
        On the UI/UX side of the project, this was my first project using Figma to build a planned design to work off of in development. Although I created a great colour scheme and consistent design system for the buttons, I had no practical experience with how a UI/UX design would realistically translate into a developed website. This resulted in a Figma prototype that formed a general idea of what the website would look like in reality - a problem when presenting ideas to the client.
        <br>
        <br>
        As a consequence of this, the client had a hard time imagining what the final project might look like. This created a prolonged back and forth between ideas, extending the ETA for the project completion significantly. Given this, I eventually was able to create a sleek and professional UI/UX design that served all the needs of Sports & Play Pack.
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
  name: 'SportsAndPlayPack',
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