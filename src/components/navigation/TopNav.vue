<template>
  <div>
    <b-navbar
      toggleable="lg"
      class="navbar-overlay navbar-inverse"
      :class="{ 'sticky-top bg-light': sticky }"
    >
      <div class="d-flex justify-content-start order-0">
        <b-navbar-brand href="#" :class="{ invisible: !sticky }"
          ><img
            src="@/assets/logo-inverse.png"
            class="d-none d-md-inline-block align-top"
            alt="Kitten"
          />
        </b-navbar-brand>
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      </div>

      <b-collapse
        id="nav-collapse"
        class="justify-content-center order-2"
        is-nav
      >
        <b-navbar-nav class="mx-auto">
          <b-nav-item
            v-for="(item, index) in navItems"
            :key="index"
            href="#"
            class="mx-3 font-weight-bold text-uppercase"
            >{{ item }}</b-nav-item
          >
        </b-navbar-nav>
      </b-collapse>

      <div class="right-item order-1 order-md-last text-right">
        <b-navbar-nav class="justify-content-end">
          <b-nav-item href="#" class="d-none d-md-block"
            ><font-awesome-icon icon="search"
          /></b-nav-item>
          <b-nav-item href="#" class="font-weight-bold">LOG IN</b-nav-item>
        </b-navbar-nav>
      </div>
    </b-navbar>
  </div>
</template>

<style lang="scss" scoped>
.navbar {
  height: 70px;
  z-index: 99;

  position: relative;
  transition: 0.2s all ease-out;

  .navbar-brand img {
    height: 50px;
  }

  &.sticky-top {
    position: fixed;
    top: 0;
    height: unset;
    width: 100%;
    margin-bottom: 0;

    .nav-link {
      color: #2d3e4f !important;
    }
  }

  &.navbar-overlay {
    margin-bottom: -70px;
  }
}

.navbar-toggler-icon,
.nav-link {
  color: #ffffff !important;
}
</style>

<script>
export default {
  data() {
    return {
      sticky: false,
      scrollPosition: null,
      navItems: ["about us", "blog", "collection", "latest news", "faq"]
    };
  },
  watch: {
    scrollPosition: function(e) {
      this.sticky = e > 70 ? true : false;
    }
  },
  mounted() {
    window.addEventListener("scroll", this.onScroll);
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.onScroll);
  },
  methods: {
    onScroll() {
      this.scrollPosition =
        window.pageYOffset || document.documentElement.scrollTop;
    }
  }
};
</script>
