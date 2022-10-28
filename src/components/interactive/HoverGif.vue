<template>

  <strong class="font-size-20 relative" @mouseover="updateCoordinates">
    {{ content }}

    <img :src="gifURL" class="rounded-xl hidden absolute lg:h-48 lg:w-64 lg:block hover-img" :style="'top:' + (y * .5) + 'px;' + 'left:' + (x * .05) + 'px;'">
  </strong>

</template>


<script lang="ts">
import { Icon } from '@iconify/vue';

export default {
  name: 'HoverGif',
  components: {

	},
  props: {
    gifURL: String,
    content: String
  },
  data() {
    return {
      x: 0,
      y: 0,
      cursorOpacity: 0,
    }
  },
  methods: {
    updateCoordinates: function(event) {
      this.x = event.clientX;
      this.y = event.clientY;
    },
  },
  // created () {

  // }
}

</script>


<style scoped lang="scss">
  @use '../../sass/abstracts' as *;
  @use '../../sass/themes' as *;

  img {
    position: absolute;
    translate: -50% -50%;
    transition: top 400ms linear, left 400ms linear, opacity 150ms linear;
    opacity: 0;
    z-index: -1;
  }

  strong:hover > img {
    opacity: 1;
  }

</style>