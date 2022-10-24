<template>
  <div class="w-full">

    <DesktopHeader :pageName="pageName" />

    <MobileHeader :pageName="pageName" />

  </div>
</template>


<script lang="ts">
import DesktopHeader from "../components/header/DesktopHeader.vue";
import MobileHeader from "../components/header/MobileHeader.vue";

export default {
    name: "Header",
    components: { DesktopHeader, MobileHeader },
    props: {
      pageName: {
        type: String
      }
    }
}

</script>


<style scoped lang="scss">
  @use '../sass/abstracts' as *;
  @use '../sass/themes' as *;



</style>