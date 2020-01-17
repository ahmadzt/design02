<template>
  <ul class="paginate">
    <li
      v-for="(page, index) in total"
      :key="index"
      :class="{
        active: current == index,
        light: type == 'light',
        dark: type == 'dark'
      }"
      @click="navigate(index)"
    ></li>
  </ul>
</template>
<style lang="scss">
.paginate {
  display: flex;
  justify-content: center;
  padding: 0;

  li {
    padding: 3px 15px;
    opacity: 0.5;
    cursor: pointer;
    margin-right: 7px;
    border-radius: 2px;
    position: relative;
    display: inline-block;
    animation: 0.3 ease-in;

    &.dark {
      background-color: black;
    }
    &.light {
      background-color: white;
    }

    &.active {
      opacity: 1;
    }
  }
}
</style>
<script>
export default {
  props: {
    total: {
      type: Number,
      default: 3
    },
    current: {
      type: Number,
      default: 0
    },
    type: {
      type: String,
      default: "light"
    }
  },
  methods: {
    navigate(index) {
      this.$emit("navigate", index);
    }
  }
};
</script>
