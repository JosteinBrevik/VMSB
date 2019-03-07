


<template>
  <div class="item" v-on:click="switchMsg()">{{msg}}</div>
</template>

<script>
export default {
  name: "itemBox",
  data() {
    return {};
  },
  props: ["msg"],
  methods: {
    switchMsg: function() {
      this.msg = "CLICK";
    }
  }
};
</script>

<style lang="scss">
.item {
  border-color: cyan;
  margin: 10px;
  padding: 20px;
  background-color: lightgrey;
  width: 200px;
  align-self: center;
}

.item:hover {
  background-color: grey;
}
</style>
