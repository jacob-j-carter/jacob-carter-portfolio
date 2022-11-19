<template>

  <img :src="cursorImg" alt="funny gif relating to text being hovered over" @mousemove="updateCoordinates" :style="'top:' + y + 'px;' + 'left:' + x + 'px;'">

</template>


<script lang="ts">
import { Icon } from '@iconify/vue';

export default {
  name: 'GifCursor',
  components: {
		Icon,
	},
  props: {
    cursorImg: String
  },
  data() {
    return {
      x: 0,
      y: 0
    }
  },
  methods: {
    updateCoordinates: function(event) {
      // pass event object, bound to mouse move with updat
      this.x = event.clientX;
      this.y = event.clientY;
    }
  }
  // created () {

  // }
}

</script>


<style scoped lang="scss">
  @use '../../sass/abstracts' as *;
  @use '../../sass/themes' as *;

  img {
    position: absolute;
    width: 10em;
    border-radius: 1em;
    translate: -50% -50%;
    top:50%;
    left:50%;
  }

</style>