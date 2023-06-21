<template>
  <button @click="clickButton">
    {{ text }}
  </button>
</template>

<script>
export default {
  props: {
    text: { type: String, default: null },
    width: { type: String, default: "200px" },
    height: { type: String, default: "50px" },
    fontSize: { type: String, default: "20px" },
    boderRadius: { type: String, default: "10px" },
  },
  emits: ["click"],
  setup(_, { emit }) {
    const clickButton = () => {
      emit("click");
    };
    return { clickButton };
  },
};
</script>

<style lang='scss' scoped>
button {
  background-color: #40407f;
  color: white;
  margin: 15px;
  width: v-bind(width);
  height: v-bind(height);
  font-size: v-bind(fontSize);
  border: none;
  border-radius: v-bind(boderRadius);
}
</style>