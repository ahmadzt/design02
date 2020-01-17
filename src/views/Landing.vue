<template>
  <div>
    <top-nav />
    <main-section />
    <second-section />
    <third-section />
    <fourth-section />
    <footer-section />
    <side-button />
  </div>
</template>

<script>
import topNav from "@/components/navigation/TopNav";
import mainSection from "@/components/landing/SectionMain";
import secondSection from "@/components/landing/SectionSecond";
import thirdSection from "@/components/landing/SectionThird";
import fourthSection from "@/components/landing/SectionFourth";
import footerSection from "@/components/navigation/Footer";
import sideButton from "@/components/buttons/SideButton";

export default {
  components: {
    topNav,
    sideButton,
    mainSection,
    secondSection,
    thirdSection,
    fourthSection,
    footerSection
  }
};
</script>
