<template>
  <div class="to-do-list">
    <div class="to-do-list__container">
      <div class="to-do-list__header">
        <h1 class="to-do-list__title">ToDo list</h1>
        <buttonComponent text="ADD" @click="addToDoItem"></buttonComponent>
      </div>
      <div class="to-do-list__checkboxes">
        <checkboxComponent
          :title="toDoItem.title"
          :subtitle="toDoItem.subtitle"
          :checked="toDoItem.isChecked"
          @input="toggle(toDoItem)"
          v-for="(toDoItem, index) in toDoItems"
          :key="index"
        />
      </div>
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
    toggle(toDoItem) {
      toDoItem.isChecked = !toDoItem.isChecked;
    },
    addToDoItem() {
      this.toDoItems.push(
        {
          title: 'Name',
          subtitle: 'Name',
          isChecked: false,
        },
      );
    },
  },
  data() {
    return {
      isChecked: false,
      toDoItems: [
        {
          title: 'Name',
          subtitle: 'Name',
          isChecked: false,
        },
        {
          title: 'Name2',
          subtitle: 'Name2',
          isChecked: false,
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "./toDoList.scss";
</style>
