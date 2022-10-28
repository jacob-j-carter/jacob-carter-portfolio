<template>

  <div :key="project.name" v-for="project in portfolioItems" class="w-full border-b-2 border-b-solid border-b-white py-4 mt-8 md:mt-16">
    <a :href="project.itemHREF" class="lg:flex lg:justify-between">
      <img :src="project.thumbnailURL" :alt="'mockup of' + project.name + 'website'" class="md:h-96 w-full lg:hidden">
      <h3 class="text-white font-size-48 my-4 lg:my-0">
        {{project.name}}
      </h3>
      <div class="flex justify-between items-center lg:items-end flex-wrap lg:flex-nowrap">
        <p :key="tag.tag" v-for="tag in project.tags" class="text-stone-300 uppercase lg:ml-4">
          {{ tag.tag }}
        </p>
      </div>
    </a>
  </div>
  
</template>


<script lang="ts">
import { Icon } from '@iconify/vue';
import portfolioItems from '../../data/portfolioItems.json'

export default {
  name: 'LibraryItems',
  components: {
		Icon,
	},
  // props: {

  // },
  data () {
    return {
      portfolioItems: portfolioItems
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