<template>
  <div class="loader wf-section" style="display: none">
    <div class="loader-wrapper">
      <div class="progress-bar-wrapper">
        <div
          class="progress-bar"
          style="
            transform: translate3d(-100%, 0px, 0px) scale3d(1, 1, 1)
              rotateX(0deg) rotateY(0deg) rotateZ(0deg) skew(0deg, 0deg);
            transform-style: preserve-3d;
          "
        ></div>
      </div>
    </div>
  </div>
  <div class="full-page">
    <Navbar></Navbar>
    <MainTitleSection></MainTitleSection>
    <AboutSection></AboutSection>
    <MarketingSection></MarketingSection>
    <CompanyInfoSection></CompanyInfoSection>
    <ParticipateSection></ParticipateSection>
    <Footer :companyLogo="companyLogo"></Footer>
  </div>
</template>

<script setup>
import Navbar from "./components/Navbar.vue";
import MainTitleSection from "./components/MainTitleSection.vue";
import AboutSection from "./components/AboutSection.vue";
import MarketingSection from "./components/MarketingSection.vue";
import CompanyInfoSection from "./components/CompanyInfoSection.vue";
import ParticipateSection from "./components/ParticipateSection.vue";
import Footer from "./components/Footer.vue";
import { ref } from "@vue/reactivity";

// Footer data
const companyLogo = ref("/assets/61f314a5cce72f5bd933270d_Friday-black.svg");
</script>

<style></style>
