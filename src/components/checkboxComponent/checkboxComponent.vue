<template>
  <div class="checkbox-list">
    <label class="checkbox-list__item" :class="{ 'checked': checked }">
      <input
        :checked="checked"
        type="checkbox"
        class="checkbox-list__item--input"
        @input="onInput"
      />
      <div class="checkbox-list__item--data">
        <span class="checkbox-list__item--text">{{title}}</span>
        <span v-if="subtitle" class="checkbox-list__item--text checkbox-list__item--text_subtitle">
          {{subtitle}}
        </span>
      </div>
    </label>
  </div>
</template>

<script>
export default {
  name: 'checkboxComponent',
  props: {
    title: {
      type: String,
      default: '',
    },
    subtitle: {
      type: String,
      default: '',
    },
    checked: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    onInput() {
      this.$emit('input', !this.checked);
    },
  },
};
</script>

<style lang="scss">
@import "./checkboxComponent.scss";
</style>
