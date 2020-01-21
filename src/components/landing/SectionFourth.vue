<template>
  <div class="fourth-section">
    <div class="background"></div>
    <div class="content position-relative">
      <b-container class="p-5">
        <b-row>
          <b-col
            lg="6"
            class="d-none d-lg-flex flex-column justify-content-center pb-2 pt-4"
          >
            <div
              v-for="(opt, index) in options"
              :key="index"
              :class="{ inactive: slide != index }"
              @click="slide = index"
              class="cursor-pointer py-2 text-left border-bottom"
            >
              <h3>{{ opt.title }}</h3>
              <p class="h4 font-weight-light">{{ opt.description }}</p>
            </div>
          </b-col>
          <b-col lg="6">
            <b-carousel
              ref="myCarousel"
              v-model="slide"
              no-animation
              no-indicators
            >
              <b-carousel-slide
                img-src="https://i.postimg.cc/Y2dbCWj3/slider-1.png"
              ></b-carousel-slide>
              <b-carousel-slide
                img-src="https://i.postimg.cc/9FSbGHdw/slider-2.png"
              ></b-carousel-slide>
              <b-carousel-slide
                img-src="https://i.postimg.cc/RVqG6ZHz/slider-3.png"
              ></b-carousel-slide>
            </b-carousel>
            <div></div>
          </b-col>
        </b-row>
      </b-container>
    </div>
  </div>
</template>

<style lang="scss">
.fourth-section {
  position: relative;
  padding-bottom: 100px;
  background-color: #f4f4f4;

  .background {
    position: absolute;
    width: 100%;
    height: 100%;
    top: -102px;
    height: 100%;
    transform: skewY(-6deg);
    background-color: #f4f4f4;
  }

  .inactive {
    opacity: 0.6;
  }

  .cursor-pointer {
    cursor: pointer;
  }
}
</style>

<script>
export default {
  components: {},
  data() {
    return {
      slide: 0,
      options: [
        {
          title: "Sed Posor Le Nanin aqua",
          description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit"
        },
        {
          title: "Sed Posor Le Nanin aqua",
          description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit"
        },
        {
          title: "Sed Posor Le Nanin aqua",
          description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit"
        }
      ]
    };
  }
};
</script>
