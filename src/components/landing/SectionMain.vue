<template>
  <div>
    <b-jumbotron class="main-section mb-0">
      <img
        src="https://i.postimg.cc/KYrhgY1T/logo.png"
        alt=""
        class="logo mb-4"
      />
      <p class="mb-5 h3 text-white font-weight-bold">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit
      </p>
      <b-button variant="primary" size="lg" href="#">Explore Now</b-button>
      <div class="position-absolute fixed-bottom mb-4">
        <paginate :current="currentPage" @navigate="navigate" />
      </div>
    </b-jumbotron>
  </div>
</template>
<style lang="scss" scoped>
.logo {
  width: 250px;
}

.main-section {
  position: relative;
  border-radius: 0;
  background-image: linear-gradient(
      0deg,
      rgba(58, 58, 58, 0.3),
      rgba(58, 58, 58, 0.3)
    ),
    url("https://i.postimg.cc/05HRSFyV/main-banner.png");
  background-size: cover;
  background-repeat: no-repeat;
  height: 100vh;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>

<script>
import paginate from "@/components/navigation/Paginate";
export default {
  components: { paginate },
  data() {
    return {
      currentPage: 0
    };
  },
  methods: {
    navigate(e) {
      this.currentPage = e;
    }
  }
};
</script>
