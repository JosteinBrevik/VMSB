


<template>
  <div id="app">
    <img src="../assets/logo.png">
    <h1>Hei</h1>
    <div v-if="seen">{{msg}}</div>
    <div id="searchBar">
      <input v-model="searchString">
      <button v-on:click="doSearch">Search</button>
      <p>You are searching: {{searchString}}</p>
      <p>You sent: {{search}}</p>
    </div>

    <itemBox/>
  </div>
</template>

<script>
import itemBox from "../components/Item";

export default {
  name: "app",
  components: {
    itemBox
  },
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
      seen: true,
      items: [{ text: "Rødvin" }, { text: "Hvitvin" }],
      searchString: "",
      search: "<<<"
    };
  },
  methods: {
    doSearch: function() {
      this.search = this.searchString;
    }
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>