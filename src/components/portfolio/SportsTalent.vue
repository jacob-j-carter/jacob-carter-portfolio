<template>

  <article class="px-4 md:px-16 wrapper">
    <PortfolioTemplate :projectIndex="4" />

    
    <section class="my-8">
      <h2 class="text-white font-size-48 my-8 md:mt-16">
        Goal of project
      </h2>
      
      <p class="text-white md:w-2/3">
        Sports Talent is a segment of Sprint Management Group that specializes in managing professional athletes. Many of their clients include Olympians, those in sports business, and many other acclaimed athletes. Sports Talent was looking for a revision of their already running website, hosted on Wordpress. Their legacy website was poorly designed and lacked good forethought in the functionality and UI/UX.
        <br>
        <br>
        My goal was to provide Sports Talent with a modernised recreation of their current website, however, due to its poor design, I found it would’ve been best to start from scratch. Sports Talent needed a homepage that would briefly explain what they offer, with a good balance between conciseness and detail. They also needed a way to automatically add new clients they would take on, with details including a bio, a headshot, region, and sport sector. To go along with this, they would need a ‘talent’ page to display all these clients, with the ability to filter them by region and sport. As an additional feature, they wanted a dedicated section to their news/blog section.
      </p>
      
      <h2 class="text-white font-size-48 my-8 md:mt-16 lg:mt-20">
        Challenges Faced
      </h2>
      
      <p class="text-white md:w-2/3">
        This was by far the greatest technical challenge I had taken so far. Firstly, this was the first website I designed that had both wireframes and hi-fi prototypes for mobile, tablet, and desktop. After a major revision to my website practices, Sports Talent was my first client that took advantage of my now-honed skills in both UI/UX and development. Creating these prototypes on all screen sizes gave the client a great idea of what I was going for with the website. Right away, the client loved my hi-fi design for the website, however, the wireframes were not as similar to the hi-fi prototypes as I would’ve liked in the end.
        <br>
        <br>
        Building the main structure and styling (with HTML and SCSS) was relatively simple, and after the hundreds of hours of experience in those two languages I had obtained over the past few months, I encountered very few problems. When it came to the components that would include JavaScript (in my case, Vue JS), this is what worried me most about this project. Having little experience in practical JavaScript and APIs, with zero experience using Vue JS, I was learning how to accomplish many of my goals along the way. This included programming a sorting system for the previously mentioned ‘talent’ page, which would sort by a dropdown of region and sport. I also needed to connect an API to a Medium blog account, that would pull the content from several news articles automatically.
        <br>
        <br>
        Fortunately for me, these challenges weren’t as big of a hurdle as I initially thought. Overall, the Sports Talent website was an easy-going process, although a lengthy one. The final product matched the hi-fi Figma prototype almost perfectly, and it ended up with no issues regarding responsiveness.
      </p>
    </section>

    <section class="md:mt-16 md:grid md:grid-cols-2">
      <div class="md:mr-2">
        <h2 class="text-white font-size-48 my-8">
          Wireframes  
        </h2>
        <img :src="'/assets/images/portfolio/sportstalent/showcase/wireframe/index.png'" :alt="'Wireframe of ' + projectName + ' website'" class="w-full">
      </div>
    
      <div class="md:ml-2">
        <h2 class="text-white font-size-48 my-8">
          Hi-Fi Prototype
        </h2>
        <img :src="'/assets/images/portfolio/sportstalent/showcase/hifi/index.png'" :alt="'Screenshot of ' + projectName + ' website'" class="w-full">
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
  name: 'SportsTalent',
  components: {
		Icon,
    PortfolioTemplate,
	},
  // props: {

  // },
  data () {
    return {
      project: portfolioItems[4],
      projectName: 'Sports Talent'
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