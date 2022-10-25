<template>
<div class="to-do-list">
  <div class="to-do-list__header">
    <h1 class="to-do-list__title">ToDo List</h1>
  <buttonComponent></buttonComponent>
  </div>
  <checkboxComponent></checkboxComponent>
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
};
</script>

<style lang="scss">
@import "./toDoList.scss";
</style>
