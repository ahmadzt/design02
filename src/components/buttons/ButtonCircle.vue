<template>
  <button class="btn-circle-lg p-3 mb-4 mb-md-0 mr-md-4">
    <font-awesome-icon :icon="icon" class="h1" />
    <p class="font-weight-bold h3">{{ title }}</p>
    <p>{{ description }}</p>
  </button>
</template>

<style lang="scss">
.btn-circle-lg {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  cursor: pointer;
  width: 300px;
  height: 300px;
  border-radius: 50%;
  border: 1px solid black;
  background-color: unset;
  transition: background-color 300ms linear;

  &:hover {
    background-color: #2d3e4f;
    color: #ffffff;
  }
}
</style>

<script>
export default {
  props: {
    icon: {
      type: String,
      default: "sliders-h"
    },
    title: {
      type: String,
      default: "Quesque ligula rutrum vel"
    },
    description: {
      type: String,
      default:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut"
    }
  }
};
</script>
