<template>

  <article class="px-4 md:px-16 wrapper">
    <PortfolioTemplate :projectIndex="2" />

    
    <section class="my-8">
      <h2 class="text-white font-size-48 my-8 md:mt-16">
        Goal of project
      </h2>
      
      <p class="text-white md:w-2/3">
        MediAid is a business that offers qualified first-aid training for organisations across the United Kingdom. Run by Vincent Staunton, MediAid has provided its training services to organisations such as the University of Liverpool, and UK Parliament. After over three decades of running MediAid, no website had been created for the business, restricting its potential market significantly. 
        <br>
        <br>
        MediAid needed a way to display its services to firms across the United Kingdom. Since MediAid predominantly worked for large business and government institutions, they needed a professional and easy-to-absorb landing page that MediAid could confidently send to potential clients.
      </p>
      
      <h2 class="text-white font-size-48 my-8 md:mt-16 lg:mt-20">
        Challenges Faced
      </h2>
      
      <p class="text-white md:w-2/3">
        Although I love building artistic websites that let me creativity flourish, I had no problem creating a digestible website for a professional client. To achieve a digestible design, I opted to creating a very consistent design system, using predominantly sans serif fonts and a small range of matching colours. To create a blithe user experience, which would be needed for a clientele consisting of professional organisations, consistent and generous spacing between sections was added to the UI design.
        <br>
        <br>
        This time around, my main focus was solidifying my practices when it came to the UI & UX design. Previously, the wireframes would never entirely match the hi-fi design, and the hi-fi design would always vary from the final product. In recent months, I had gotten significantly better at replicating the hi-fi design in development, getting to the point where projects would align pixel-to-pixel from the hi-fi design to the final website. My focus for MediAid’s website was to improve my wireframing process. I had never taken on any consistent practice when designing the initial wireframe, and would often not put much thought into the process. For this project, I started the project by physically sketching out a wireframe for the website (like the good ol’ days). After doing this, I replicated the wireframe in Figma with a more professional (and less ugly) look. For the wireframes, I opted to use only a few premade wireframe components, to make the overall wireframe more consistent, as well as saving the copy till I work on the high fidelity design.
        <br>
        <br>
        From the simplicity of the overall goal, MediAid’s website didn’t bring me many technical challenges; the UI & UX designing stage took ~4 days, and the development only took me 3 days. Overall, this was a very pleasant experience.
      </p>
    </section>

    <section class="md:mt-16 md:grid md:grid-cols-2">
      <div class="md:mr-2">
        <h2 class="text-white font-size-48 my-8">
          Wireframes  
        </h2>
        <img :src="'/assets/images/portfolio/mediaid/showcase/wireframe/lg/index.png'" :alt="'Wireframe of ' + projectName + ' website'" class="w-full">
      </div>
    
      <div class="md:ml-2">
        <h2 class="text-white font-size-48 my-8">
          Hi-Fi Design
        </h2>
        <img :src="'/assets/images/portfolio/mediaid/showcase/hifi/lg/index.png'" :alt="'Screenshot of ' + projectName + ' website'" class="w-full">
      </div>
    </section>

    <div class="flex justify-end w-full mt-8 md:mt-16">
      <a :href="project.websiteURL" :title="'website of ' + projectName" target="_blank">
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
  name: 'MediAid',
  components: {
		Icon,
    PortfolioTemplate,
	},
  // props: {

  // },
  data () {
    return {
      project: portfolioItems[2],
      projectName: 'MediAid',
      projectLink: 'mediaid',
    }
  },
  // methods: {

  // },
}

</script>


<style scoped lang="scss">
  @use '../../sass/abstracts' as *;
  @use '../../sass/themes' as *;



</style>