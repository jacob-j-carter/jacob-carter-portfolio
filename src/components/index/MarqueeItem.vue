<template>

  <h2 class="text-center uppercase body-font font-bold font-size-16">
    {{ marqueeItem }} 
    <i class="fa-solid fa-circle-dot mx-8"></i>
  </h2>

</template>


<script lang="ts">

export default {
  name: 'MarqueeItem',
  props: {
    marqueeItem: {
      type: String,
      default: 'Item'
    }
  }
}

</script>


<style scoped lang="scss">


</style>