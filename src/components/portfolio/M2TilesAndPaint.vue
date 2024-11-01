<template>

  <article class="px-4 md:px-16 wrapper">
    <PortfolioTemplate :projectIndex="0" />

    
    <section class="my-8">
      <h2 class="text-white font-size-48 my-8 md:mt-16">
        Goal of project
      </h2>
      
      <p class="text-white md:w-2/3">
        I worked in the M2 Tiles & Paint showroom/store between 12th June 2021 and 13th August 2022. When I joined, the store eCommerce website had been developed by a third-party on Shopify. Although the functionality of the eCommerce site was on par with what M2 Tiles & Paint needed at the time, the UI and UX were very poor. This was a substantial issue for the store, as it marketed itself as a place to get practical and professional design advice for the homes of customers; having a bland, unappealing website negatively impacted the public image of M2 Tiles & Paint significantly.
        <br>
        <br>
        Thankfully, most of the technical functionality of the website had already been setup (aside from a few incorrect product details). Shopify provides a good deal of aesthetic choices, while keeping the process of building a website relatively simple. Given this information, I decided to start the website from scratch between breaks from talking to customers.
        <br>
        <br>
        Immediately, my design provided a much better representation of the business. My keen eye for detail provided the online store with a beautiful look and feel - going from a dull white and green colour scheme, to a vibrant range of hue, given in large part by the store’s wide selection of gorgeous paints and tiles.
        <br>
        <br>
        Later in the process, I connected Google Analytics to the website, which demonstrated to M2 Tiles & Paint where marketing resources should be focussed.
      </p>
      
      <h2 class="text-white font-size-48 my-8 md:mt-16 lg:mt-20">
        Challenges Faced
      </h2>
      
      <p class="text-white md:w-2/3">
        As Shopify does most of the technical work for you, building the M2 Tiles & Paint website wasn’t a huge hurdle. The larger problem came with the sheer scale of the website. M2 Tiles & Paint is a stockist of multiple suppliers from across Europe - totalling 18,000+ products that would be displayed on the website. Using a .csv Microsoft Excel file, I manually documented all products with appropriate descriptions, prices, images, tags and more.
        <br>
        <br>
        Being the first large web project, M2 Tiles & Paint gave me the motivation and knowledge to begin my front-end engineering career. Although it wasn’t a huge technical challenge, knowing that I could effectively create a beautiful web design that would perfectly match the businesses brand identity led me to kickstart my freelance work, and later found Choice Digital Studio. 
      </p>
    </section>

    <section class="md:mt-16 md:grid md:grid-cols-2">
      <div class="md:mr-2">
        <h2 class="text-white font-size-48 my-8">
          Homepage  
        </h2>
        <img :src="'/assets/images/portfolio/m2tilesandpaint/showcase/final/homepage.png'" :alt="'Screenshot of ' + projectName + ' homepage'" class="w-full">
      </div>
      <div class="md:mr-2 ">
        <h2 class="text-white font-size-48 my-8">
          Blog  
        </h2>
        <img :src="'/assets/images/portfolio/m2tilesandpaint/showcase/final/blog.png'" :alt="'Screenshot of ' + projectName + ' blog'" class="w-full">
      </div>
      <div class="md:mr-2">
        <h2 class="text-white font-size-48 my-8">
          Paint Store 
        </h2>
        <img :src="'/assets/images/portfolio/m2tilesandpaint/showcase/final/paint.png'" :alt="'Screenshot of ' + projectName + ' paint shop'" class="w-full">
      </div>

    </section>

  </article>
  
  

</template>


<script lang="ts">
import { Icon } from '@iconify/vue';
import PortfolioTemplate from './PortfolioTemplate.vue';
import portfolioItems from '../../data/portfolioItems.json'

export default {
  name: 'M2 Tiles & Paint',
  components: {
		Icon,
    PortfolioTemplate,
	},
  // props: {

  // },
  data () {
    return {
      project: portfolioItems[0],
      projectName: 'M2 Tiles & Paint',
      projectLink: 'm2tilesandpaint',
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