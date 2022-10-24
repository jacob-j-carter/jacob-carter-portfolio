<template>
  <a :href="HREF">
    <button :class="[span ? 'span' : '']" class="py-4 px-8 rounded-xl text-white">
      {{ content }}
    </button>
  </a>
</template>


<script lang="ts">

export default {
  name: 'Placeholder',
  props: {
    HREF: {
      type: String,
      default: '/'
    },
    content: {
      type: String,
      default: 'Button Text'
    },
    span: {
      type: Boolean,
      default: false
    },
  }
}

</script>


<style scoped lang="scss">
  @use '../../sass/abstracts' as *;
  @use '../../sass/themes' as *;

  button {
    background-color: $primary-50;
    font-family: $button-font;
    font-weight: 700;
    cursor: pointer;
    

    &:hover {
      background-color: $primary-60;
    }
  }

  .span {
    width: 100%;
  }

</style>