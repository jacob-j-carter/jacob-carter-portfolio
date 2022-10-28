<template>

  <div :key="project.name" v-for="project in portfolioItems" class="w-full border-b-2 border-b-solid border-b-white py-4 mt-8 md:mt-16" @mouseover="updateCoordinates">
    <a :href="project.itemHREF" class="lg:flex lg:justify-between relative">
      <img :src="project.thumbnailURL" :alt="'mockup of' + project.name + 'website'" class="md:h-96 w-full lg:hidden">
      <img :src="project.thumbnailURL" :alt="'mockup of' + project.name + 'website'" class="rounded-xl hidden absolute lg:h-48 lg:w-64 lg:block hover-img" :style="'top:' + (y * .05) + 'px;' + 'left:' + (x * .65) + 'px;'">
      <h3 class="text-white font-size-48 my-4 lg:my-0" >
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
  data() {
    return {
      x: 500,
      y: 350,
      cursorOpacity: 0,
      portfolioItems: portfolioItems
    }
  },
  methods: {
    updateCoordinates: function(event) {
      this.x = event.clientX;
      this.y = event.clientY;
    },
  }
  // created () {

  // }
}

</script>


<style scoped lang="scss">
  @use '../../sass/abstracts' as *;
  @use '../../sass/themes' as *;

  .hover-img {
    position: absolute;
    translate: -50% -50%;
    transition: top 400ms linear, left 400ms linear, opacity 150ms linear;
    opacity: 0;
    z-index: -1;
  }

  a:hover > .hover-img {
    opacity: 1;
  }

</style>