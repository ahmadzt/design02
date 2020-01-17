<template>
  <div class="side-button d-none d-md-flex">
    <div class="side-item flex p-3 my-1">
      <font-awesome-icon icon="exclamation-circle" size="lg" class="mr-3" />
      <span class="text-uppercase">cta button</span>
    </div>
    <div class="side-item flex p-3">
      <font-awesome-icon icon="sliders-h" size="lg" class="mr-3" />
      <span class="text-uppercase">view sample</span>
    </div>
  </div>
</template>

<style lang="scss">
.side-button {
  position: fixed;
  bottom: 20%;
  right: 0;
  z-index: 5;

  flex-direction: column;

  .side-item {
    background-color: rgba(103, 109, 109, 0.637);
    transition: 0.2s all ease-out;
    color: #ffffff;
    cursor: pointer;

    &:hover {
      background-color: rgba(202, 149, 44, 0.774);
    }
  }
}
</style>
