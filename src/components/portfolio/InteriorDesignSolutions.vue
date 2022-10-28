<template>

  <article class="px-4 md:px-16 wrapper">
    <PortfolioTemplate :projectIndex="2" />

    
    <section class="my-8">
      <h2 class="text-white font-size-48 my-8 md:mt-16">
        Goal of project
      </h2>
      
      <p class="text-white md:w-2/3">
        Interior Design Solutions is an upcoming interior design company based in Mojacar, Spain. They specialise in crafting gorgeous bespoke interiors for clients in Spain and Britain. IDS needed a unique website that would reflect their European origins and stunning design talent. They were looking for a ‘rustic’ look , with the appearance of a mood board; having pinned photos and textiles animate in. 
        <br>
        <br>
        In the Figma prototype, IDS were thrilled with the design concept I came up with. It featured warm colours with a cross-stitch background to symbolise both European brick roads and woven fabric.
      </p>
      
      <h2 class="text-white font-size-48 my-8 md:mt-16 lg:mt-20">
        Challenges Faced
      </h2>
      
      <p class="text-white md:w-2/3">
        Although the UI/UX design was great in theory, translating that into a functioning website was an incredibly arduous process. The prototype did not at all account for differing screen sizes, making responsiveness and accessibility of poor quality.
        <br>
        <br>
        The key challenge I faced was that I was using WordPress for something WordPress was not at all built for. My ambition for this project ended up surpassing what I or my website builder was technically capable of doing.
        <br>
        <br>
        While this was the case, I still managed to deliver a website that, overall, matched the aesthetic I was going for. The client was very happy with the final product.
      </p>
    </section>

    <section class="md:mt-16 md:grid md:grid-cols-2">
      <div class="md:mr-2">
        <h2 class="text-white font-size-48 my-8">
          Wireframes  
        </h2>
        <img :src="'/assets/images/portfolio/interiordesignsolutions/showcase/wireframe/index.png'" :alt="'Wireframe of ' + projectName + ' website'" class="w-full">
      </div>
    
      <div class="md:ml-2">
        <h2 class="text-white font-size-48 my-8">
          Final Product
        </h2>
        <img :src="'/assets/images/portfolio/interiordesignsolutions/showcase/final/index.png'" :alt="'Screenshot of ' + projectName + ' website'" class="w-full">
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
      project: portfolioItems[2],
      projectName: 'Interior Design Solutions',
      projectLink: 'interiordesignsolutions',
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