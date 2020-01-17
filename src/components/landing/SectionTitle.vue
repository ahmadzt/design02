<template>
  <div
    class="section-title d-flex flex-column justify-content-center"
    :class="{ light: type == 'light' }"
  >
    <p class="mb-0 text-uppercase pt-4 h4">{{ name }}</p>
    <h1 class="mt-2 mb-0 font-weight-bold text-uppercase">{{ title }}</h1>
  </div>
</template>

<style lang="scss">
.section-title {
  p {
    position: relative;

    &::before {
      content: "";
      position: absolute;
      top: 0;
      right: 0;
      left: 0;
      margin: 0 auto;
      width: 100px;
      border: 4px solid #2d3e4f;
    }
  }

  &.light {
    color: #ffffff;

    p {
      &::before {
        border-color: #ffffff;
      }
    }
  }
}
</style>

<script>
export default {
  props: {
    type: {
      type: String,
      default: "dark"
    },
    name: {
      type: String,
      default: "section name"
    },
    title: {
      type: String,
      default: "section title"
    }
  }
};
</script>
