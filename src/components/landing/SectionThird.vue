<template>
  <div class="third-section">
    <div class="background"></div>
    <div class="content">
      <b-container class="p-5">
        <div>
          <section-title
            name="about us"
            title="curabitur nisl lorem"
            type="light"
          />
          <div class="d-flex justify-content-center mt-4 mb-5">
            <div
              class="d-flex flex-column flex-lg-row justify-content-center text-white bg-dark-custom"
            >
              <div class="text-center p-4">
                <p class="font-weight-bold text-capitalize">Date</p>
                <p>23rd Jun - 1st July 2019</p>
              </div>
              <div class="text-center p-4">
                <p class="font-weight-bold text-capitalize">Venue</p>
                <p>Lorem ipsum dolor sit amet, consectetur</p>
              </div>
              <div class="text-center p-4">
                <p class="font-weight-bold text-capitalize">Time</p>
                <p>Mon - Fri: 0900AM - 0500PM</p>
                <p>Mon - Fri: 0900AM - 0500PM</p>
              </div>
            </div>
          </div>

          <div class="d-flex flex-column flex-lg-row justify-content-center">
            <blogCard
              v-for="(blog, index) in blogPost"
              :key="index"
              :title="blog.title"
              :description="blog.description"
              class="col"
            />
          </div>
        </div>
      </b-container>
    </div>
  </div>
</template>

<style lang="scss">
.third-section {
  padding-top: 150px;
  padding-bottom: 300px;
  position: relative;
  background-image: linear-gradient(
      0deg,
      rgba(0, 0, 0, 0.6),
      rgba(0, 0, 0, 0.6)
    ),
    url("./../../assets/second_banner.png");
  background-size: cover;

  .bg-dark-custom {
    background-color: rgba(0, 0, 0, 0.7);
  }
}
</style>

<script>
import sectionTitle from "@/components/landing/SectionTitle";
import blogCard from "@/components/landing/BlogCard";

export default {
  components: {
    blogCard,
    sectionTitle
  },
  data() {
    return {
      blogPost: [
        {
          title: "curab nisl lorem",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua"
        },
        {
          title: "curabitur nisl",
          description:
            "Lorem ipsum dolor sit amet, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua"
        },
        {
          title: "curab jala lorem",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing ut labore et dolore magna aliqua"
        }
      ]
    };
  }
};
</script>
