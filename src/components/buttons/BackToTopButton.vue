<template>
  <button class="back-top-btn" @click="scrollTop()">
    <font-awesome-icon icon="caret-up" class="text-white h2 mb-0" />
  </button>
</template>

<style lang="scss">
.back-top-btn {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: black;

  position: absolute;
  top: -60px;
  right: 30px;
}
</style>

<script>
export default {
  methods: {
    scrollTop() {
      // eslint-disable-next-line no-console
      console.log(window);
      window.scrollTo(0, 0);
    }
  }
};
</script>
