<template>

  <article class="wrapper px-4">
    <div class="w-full border-b-2 border-b-solid border-b-white py-4 mt-32">
      <a :href="project.itemHREF">
        <img :src="project.thumbnailURL" :alt="'mockup of' + project.name + 'website'">
        <h1 class="text-white my-4 font-size-56">
          {{project.name}}
        </h1>
        <div class="flex justify-between items-center flex-wrap">
          <p :key="tag.tag" v-for="tag in project.tags" class="text-stone-300 uppercase">
            {{ tag.tag }}
          </p>
        </div>
      </a>
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