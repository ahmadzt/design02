<template>
  <div class="footer bg-dark text-white position-relative">
    <b-container fluid>
      <b-row>
        <b-col cols="auto" class="mr-auto py-2 p-md-3 px-5">
          <small>
            <a href="" class="text-white">Privacy Policy</a>
            <span class="mx-2">|</span>
            <a href="" class="text-white">Terms of Use</a>
          </small>
        </b-col>
        <b-col cols="auto" class="py-2 p-md-3 px-5">
          <small class="text-white">Copyright Ⓒ2018. All rights reserved</small>
        </b-col>
      </b-row>
    </b-container>
    <back-top-btn />
  </div>
</template>

<script>
import backTopBtn from "@/components/buttons/BackToTopButton";
export default {
  components: { backTopBtn }
};
</script>
