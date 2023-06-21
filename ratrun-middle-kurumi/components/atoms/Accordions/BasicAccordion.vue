<template>
  <div class="title">
    <button @click="clickButton">
      <p>{{ title }}</p>
      <p>＋</p>
    </button>
    <div class="description" v-show="isAccordion">
      <p>{{ description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: { type: String, default: null },
    description: { type: String, default: null },
  },
  emits: ["click"],
  setup(_, { emit }) {
    const isAccordion = ref(false);
    const clickButton = () => {
      isAccordion.value = !isAccordion.value;
    };
    return { clickButton, isAccordion };
  },
};
</script>

<style lang='scss' scoped>
.title {
  align-items: center;
}
button {
  display: flex;
  margin: 0 auto;
  margin-top: 30px;
  width: 900px;
  height: 50px;
  background-color: #666666;
  color: white;
  border: none;
  justify-content: space-between;
  align-items: center;
  p {
    font-size: 25px;
  }
}

.description {
  margin: 0 auto;
  background-color: #cccccc;
  width: 900px;
  height: 100px;
  p {
    font-size: 14px;
    padding: 10px;
  }
}
</style>