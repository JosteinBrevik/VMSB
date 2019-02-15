<template>
  <div class="item">DETTE ER EN ITEM</div>
</template>

<script>
export default {
  name: "itemBox",
  data() {
    return {};
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
