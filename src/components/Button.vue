<template>
  <button @click="onClick()" v-bind:style="{background: color}">{{text}}</button>
</template>

<script>
export default {
  name: "Button",
  props: {
    text: String,
    color: String
  },
  methods: {
    onClick() {
      this.$emit("btn-click");
    }
  }
};
</script>


<style scoped >
button {
  background-color: black;
  border-radius: 10px;
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  font-size: 16px;
  cursor: pointer;
}
</style>