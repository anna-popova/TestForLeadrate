<template>
  <div id="app">
    <toDoList></toDoList>
    <authorComponent></authorComponent>
  </div>
</template>

<script>
import toDoList from './components/toDoList/toDoList.vue';
import authorComponent from './components/authorComponent/authorComponent.vue';

export default {
  name: 'App',
  components: {
    toDoList,
    authorComponent,
  },
};
</script>

<style lang="scss">
@import "./components/globalStyles.scss";
</style>
