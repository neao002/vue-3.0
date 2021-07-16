<template>
  <header>
    <h1>{{ tittle }}</h1>
    <Button @click="onCLick()" text="buttons" color="blue" />
  </header>
</template>

<script>
import Button from "./button.vue";
export default {
  name: "Header",
  props: {
    tittle: String,
  },
  components: {
    Button,
  },
  methods: {
    onCLick() {
      console.log("click");
    },
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
