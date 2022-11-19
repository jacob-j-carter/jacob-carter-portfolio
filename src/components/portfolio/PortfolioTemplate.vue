<template>

  <article>
    <div class="w-full border-b-2 border-b-solid border-b-white py-4 mt-32 lg:mt-16 lg:mb-24">
      <img :src="project.thumbnailURL" :alt="'mockup of' + project.name + 'website'" class="w-full md:h-96">
      <h1 class="text-white my-4 font-size-56">
        {{project.name}}
      </h1>
      <div class="flex justify-between items-center flex-wrap">
        <p :key="tag.tag" v-for="tag in project.tags" class="text-stone-300 uppercase">
          {{ tag.tag }}
        </p>
      </div>
    </div>

    
  </article>

</template>


<script lang="ts">
import { Icon } from '@iconify/vue';
import portfolioItems from '../../data/portfolioItems.json'


export default {
  name: 'PortfolioTemplate',
  components: {
		Icon,
	},
  props: {
    projectIndex: {
      type: Number,
      default: 0
    },
    goalContent: {
      type: String,
    },
    challengesContent: {
      type: String,
    }
  },
  data () {
    return {
      project: portfolioItems[this.projectIndex]
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