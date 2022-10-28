<template>
  <button class="button" @click="onClick">{{text}}</button>
</template>

<script>
export default {
  name: 'buttonComponent',
  props: {
    text: {
      type: String,
      default: '',
    },
  },
  methods: {
    onClick() {
      this.$emit('click');
    },
  },
};
</script>

<style lang="scss">
@import "./buttonComponent.scss";
</style>
