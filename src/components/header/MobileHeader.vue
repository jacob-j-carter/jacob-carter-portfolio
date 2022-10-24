<template>
  <div class="lg:hidden w-full">

    <MobileButtons @toggle-menu="toggleMenu()"/>

    <BurgerMenu @close-nav="toggleMenu()" :pageName="pageName" :navHidden="navHidden"/>

  </div>
</template>


<script lang="ts">
import BurgerMenu from './BurgerMenu.vue';
import MobileButtons from './MobileButtons.vue';

export default {
    name: "MobileHeader",
    components: { BurgerMenu, MobileButtons },
    props: {
      pageName: {
        type: String
      }
    },
    data () {
      return {
        navHidden: true,
      }
    },
    methods: {
      toggleMenu() {
        console.log("yesss")
        this.navHidden = !this.navHidden
      }
    },

}

</script>


<style scoped lang="scss">
  @use '../../sass/abstracts' as *;
  @use '../../sass/themes' as *;



</style>