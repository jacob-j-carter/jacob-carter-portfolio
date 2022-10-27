<template>

  <article class="px-4 wrapper">
    <PortfolioTemplate :projectIndex="1" />

    
    <h2 class="text-white font-size-48 my-8">
      Goal of project
    </h2>
    
    <p class="text-white">
      After a couple of weeks learning HTML and CSS, I regularly struggled to remember CSS flexbox, which would frustrate me endlessly when buildings layouts. I decided that the best way to effectively learn flexbox was to build a project focused entirely on the given subject.
      <br>
      <br>
      I wanted a website that would display the most common flexbox properties, as well as the most common values for such properties. A text animation would cycle through these values, displaying an appropriate graphic to go alongside it. My goal was to regularly use the website for reference when building future projects, which I (and others) eventually did.
    </p>
    
    <h2 class="text-white font-size-48 my-8">
      Challenges Faced
    </h2>
    
    <p class="text-white">
      More than any previous client project, I managed to design a wireframe and hi-fi Figma prototype that was almost identical to the final product. Being a relatively simple project, there weren’t many technical hiccoughs. However, my problems came about when trying to deploy the website.
      <br>
      <br>
      Without the knowledge I have now of front-end website deployment services, such as Netlify and Vercel, my only obvious option at the time was to create a custom WordPress theme for CSS Display Info. Creating a WordPress theme took an unnecessary amount of time to learn and develop, though it gave me some beginner knowledge into PHP.
      <br>
      <br>
      This was also my first encounter with browser support issues. I learnt after publishing the website, through a comment on Reddit, that the websites UI had been terribly disfigured on Mozilla Firefox. I later found out that some of the methods of importing fonts, animations, and the blur property had differing levels of support to other browsers, such as Chrome and Opera. I later fixed these discrepancies when I moved from WordPress to Netlify.
    </p>

    <h2 class="text-white font-size-48 my-8">
      Wireframes
    </h2>
    <img :src="'/assets/images/portfolio/' + projectLink + '/showcase/wireframe/index.png'" :alt="'Wireframe of ' + projectName + ' website'" class="w-full">
  
    <h2 class="text-white font-size-48 my-8">
      Final Product
    </h2>
    <img :src="'/assets/images/portfolio/' + projectLink + '/showcase/final/index.png'" :alt="'Screenshot of ' + projectName + ' website'" class="w-full">
  </article>
  
  

</template>


<script lang="ts">
import { Icon } from '@iconify/vue';
import PortfolioTemplate from './PortfolioTemplate.vue';

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
      projectName: 'CSS Display Info',
      projectLink: 'cssdisplayinfo'
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