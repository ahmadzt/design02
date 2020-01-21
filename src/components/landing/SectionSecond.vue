<template>
  <div class="second-section">
    <b-container class="p-5">
      <div>
        <section-title name="about us" title="curabitur nisl lorem" />
        <div class="btn-custom-group my-4">
          <button
            class="corner-button"
            :class="{ active: slide == 0 }"
            @click="slide = 0"
          >
            <span>SOLLICOTUDIN</span>
          </button>
          <button
            class="corner-button"
            :class="{ active: slide == 1 }"
            @click="slide = 1"
          >
            <span>EU VIVERRA</span>
          </button>
          <button
            class="corner-button"
            :class="{ active: slide == 2 }"
            @click="slide = 2"
          >
            <span>VENETIS VARIUS</span>
          </button>
        </div>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua
        </p>
        <b-carousel id="carousel-1" v-model="slide" :interval="4000" indicators>
          <b-carousel-slide><carousel-item /></b-carousel-slide>
          <b-carousel-slide><carousel-item /></b-carousel-slide>
          <b-carousel-slide><carousel-item /></b-carousel-slide>
        </b-carousel>
      </div>
    </b-container>
  </div>
</template>

<style lang="scss">
$bg-orange: #fdb935;

.second-section {
  background-color: #{$bg-orange};
  position: relative;

  .carousel-caption {
    position: unset;
  }

  &:after {
    content: "";
    z-index: 1;
    position: absolute;
    top: 100%;
    right: 0;
    width: 100%;
    height: 150px;
    background-color: #fdb935;
    clip-path: polygon(100% 0, 0 0, 100% 100%);
  }
}

.corner-button,
.corner-button span {
  &:before,
  &:after {
    display: block;
    content: "";
    width: 15px;
    height: 15px;
    position: absolute;
  }

  &.active {
    color: #ffffff;
    background-color: black;
  }
}

.corner-button {
  display: inline-block;
  position: relative;
  border: 1px solid black;
  text-decoration: none;
  cursor: pointer;
  padding: 1rem 20px;
  text-align: center;
  background-color: #{$bg-orange};

  &:before {
    top: -2px;
    left: -2px;
    border-top: 1px solid #ffffff;
    border-left: 1px solid #ffffff;
    transition: 0.5s all;
  }
  &:after {
    top: -2px;
    right: -2px;
    border-top: 1px solid #ffffff;
    border-right: 1px solid #ffffff;
    transition: 0.5s all;
  }
  span {
    display: block;
    &:before {
      bottom: -2px;
      left: -2px;
      border-bottom: 1px solid #ffffff;
      border-left: 1px solid #ffffff;
      transition: 0.5s all;
    }
    &:after {
      bottom: -2px;
      right: -2px;
      border-bottom: 1px solid #ffffff;
      border-right: 1px solid #ffffff;
      transition: 0.5s all;
    }
  }
  &:hover {
    color: #ffffff;
    background-color: black;
  }
}
</style>

<script>
import sectionTitle from "@/components/landing/SectionTitle";
import carouselItem from "@/components/landing/CarouselItemTwo";

export default {
  components: {
    sectionTitle,
    carouselItem
  },
  data() {
    return {
      slide: 0
    };
  }
};
</script>
