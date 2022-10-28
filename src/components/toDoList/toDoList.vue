<template>
  <div class="to-do-list">
    <div class="to-do-list__container">
      <div class="to-do-list__header">
        <h1 class="to-do-list__title">ToDo list</h1>
        <buttonComponent></buttonComponent>
      </div>
      <checkboxComponent
        title="Задача"
        subtitle="Подзадача"
        :checked="isChecked"
        @input="toggle"
      />
    </div>
    <div class="to-do-list__black-block"></div>
    <div class="to-do-list__blue-block"></div>
  </div>
</template>

<script>
import checkboxComponent from '../checkboxComponent/checkboxComponent.vue';
import buttonComponent from '../buttonComponent/buttonComponent.vue';

export default {
  name: 'toDoList',
  components: {
    checkboxComponent,
    buttonComponent,
  },
  methods: {
    toggle(value) {
      this.isChecked = value;
    },
  },
  data() {
    return {
      isChecked: false,
    };
  },
};
</script>

<style lang="scss">
@import "./toDoList.scss";
</style>
