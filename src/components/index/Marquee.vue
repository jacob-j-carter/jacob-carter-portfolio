<template>
  <section class="bg-white h-8 flex items-center mt-36">
    <div class="flex items-center relative marquee-text-div" id="marquee-one">
      <MarqueeItem :marqueeItem="'UI/UX'" />
      <MarqueeItem :marqueeItem="'Front-End Development'" />
      <MarqueeItem :marqueeItem="'CSS'" />
      <MarqueeItem :marqueeItem="'Figma'" />
      <MarqueeItem :marqueeItem="'Vue JS'" />
      <MarqueeItem :marqueeItem="'Wireframes'" />
      <MarqueeItem :marqueeItem="'HTML'" />
      <MarqueeItem :marqueeItem="'SCSS'" />
      <MarqueeItem :marqueeItem="'JavaScript'" />
      <MarqueeItem :marqueeItem="'UI/UX'" />
      <MarqueeItem :marqueeItem="'Front-End Development'" />
      <MarqueeItem :marqueeItem="'CSS'" />
      <MarqueeItem :marqueeItem="'Figma'" />
      <MarqueeItem :marqueeItem="'Vue JS'" />
      <MarqueeItem :marqueeItem="'Wireframes'" />
      <MarqueeItem :marqueeItem="'HTML'" />
      <MarqueeItem :marqueeItem="'SCSS'" />
      <MarqueeItem :marqueeItem="'JavaScript'" />



    </div>
  </section>
</template>


<script lang="ts">
import MarqueeItem from './MarqueeItem.vue';
export default {
  name: 'Marquee',
  components: {
    MarqueeItem
}
}
</script>


<style scoped lang="scss">
  
  .marquee-text-div {
    white-space: nowrap;
    animation: marquee 20s linear infinite;
  }
  @keyframes marquee {
    from { transform: translateX(0); }
    to { transform: translateX(-50%); }
  }
  section {
    rotate: -5deg;
    width: 105%;
    margin-left: -.5em;
    overflow: clip;
  }
</style>