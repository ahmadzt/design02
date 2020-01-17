<template>
  <div
    class="blog-card d-flex flex-column text-white mb-5 mb-md-0 mx-md-4 p-5 position-relative"
  >
    <span class="date px-3 py-2 font-weight-bold">{{ date }}</span>
    <h3 class="h-50 font-weight-bold">{{ title }}</h3>
    <div class="flex-fill d-flex flex-column align-items-between">
      <p v-html="description"></p>
      <a
        href=""
        class="d-flex align-items-center justify-content-center text-white"
      >
        <span class="mr-2">Read More</span>
        <font-awesome-icon icon="arrow-right" size="xs" />
      </a>
    </div>
  </div>
</template>

<style lang="scss">
.blog-card {
  background-color: rgba(0, 0, 0, 0.7);

  .date {
    position: absolute;
    top: -18px;
    left: 0;
    right: 0;
    font-size: 1rem;
    margin: 0 auto;
    color: black;
    width: 50%;
    background-color: #fdb935;
  }
}
</style>

<script>
export default {
  props: {
    title: {
      type: String,
      default: "title"
    },
    description: {
      type: String,
      default:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua"
    },
    date: {
      type: String,
      default: "01 Jan 2019"
    }
  }
};
</script>
