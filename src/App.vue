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
    <Footer
      :companyLogo="footer.companyLogo"
      :companyDescription="footer.companyDescription"
      :footerLists="footer.footerLists"
      :socialMediaLinks="footer.socialMediaLinks"
      :companyName="footer.companyName"
      :creatorCompany="footer.creatorCompany"
      :creatorCompanyWebsite="footer.creatorCompanyWebsite"
      :creatorName="footer.creatorName"
      :creatorLink="footer.creatorLink"
    ></Footer>
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
// const companyLogo = ref("/assets/61f314a5cce72f5bd933270d_Friday-black.svg");
const footer = ref({
  companyLogo: "/assets/61f314a5cce72f5bd933270d_Friday-black.svg",
  companyDescription:
    "Friday Festival is a modern Webflow Template for conference & event websites",
  footerLists: [
    {
      footerListName: "Landings",
      footerSubLists: [
        {
          footerSubListName: "Landing 01",
          sublistLink: "https://friday-template.webflow.io/landing/01",
        },
        {
          footerSubListName: "Landing 02",
          sublistLink: "https://friday-template.webflow.io/landing/02",
        },
        {
          footerSubListName: "Landing 03",
          sublistLink: "https://friday-template.webflow.io/landing/03",
        },
        {
          footerSubListName: "Landing 04",
          sublistLink: "https://friday-template.webflow.io/landing/04",
        },
        {
          footerSubListName: "Landing 05",
          sublistLink: "https://friday-template.webflow.io/landing/05",
        },
      ],
    },
    {
      footerListName: "Features",
      footerSubLists: [
        {
          footerSubListName: "Features 01",
          sublistLink: "https://friday-template.webflow.io/features/01",
        },
        {
          footerSubListName: "Features 02",
          sublistLink: "https://friday-template.webflow.io/features/02",
        },
        {
          footerSubListName: "Features 03",
          sublistLink: "https://friday-template.webflow.io/features/03",
        },
        {
          footerSubListName: "Features 04",
          sublistLink: "https://friday-template.webflow.io/features/04",
        },
        {
          footerSubListName: "Features 05",
          sublistLink: "https://friday-template.webflow.io/features/05",
        },
      ],
    },
    {
      footerListName: "CMS",
      footerSubLists: [
        {
          footerSubListName: "CMS 01",
          sublistLink: "https://friday-template.webflow.io/cms/cms-01",
        },
        {
          footerSubListName: "CMS 02",
          sublistLink: "https://friday-template.webflow.io/cms/cms-02",
        },
        {
          footerSubListName: "CMS 03",
          sublistLink: "https://friday-template.webflow.io/cms/cms-03",
        },
        {
          footerSubListName: "CMS 04",
          sublistLink: "https://friday-template.webflow.io/cms/cms-04",
        },
        {
          footerSubListName: "CMS 05",
          sublistLink: "https://friday-template.webflow.io/cms/cms-05",
        },
      ],
    },
    {
      footerListName: "Form",
      footerSubLists: [
        {
          footerSubListName: "Form 01",
          sublistLink: "https://friday-template.webflow.io/other-pages/form-01",
        },
        {
          footerSubListName: "Form 02",
          sublistLink: "https://friday-template.webflow.io/other-pages/form-02",
        },
        {
          footerSubListName: "Form 03",
          sublistLink: "https://friday-template.webflow.io/other-pages/form-03",
        },
        {
          footerSubListName: "Form 04",
          sublistLink: "https://friday-template.webflow.io/other-pages/form-04",
        },
        {
          footerSubListName: "Form 05",
          sublistLink: "https://friday-template.webflow.io/other-pages/form-05",
        },
      ],
    },
    {
      footerListName: "Template",
      footerSubLists: [
        {
          footerSubListName: "Styleguide",
          sublistLink: "https://friday-template.webflow.io/utility/style-guide",
        },
        {
          footerSubListName: "License",
          sublistLink: "https://friday-template.webflow.io/utility/licenses",
        },
        {
          footerSubListName: "Changelog",
          sublistLink: "https://friday-template.webflow.io/utility/change-log",
        },
      ],
    },
  ],
  socialMediaLinks: [
    {
      link: "https://friday-template.webflow.io/landing/01#",
      image: "/assets/61e5bb75ba3a7edc0f0bd4a4_icon-facebook.svg",
    },
    {
      link: "https://friday-template.webflow.io/landing/01#",
      image: "/assets/61e5bb75ba3a7e5ded0bd4a5_icon-instagram.svg",
    },
    {
      link: "https://friday-template.webflow.io/landing/01#",
      image: "/assets/61e5bb75ba3a7ee67e0bd4a2_icon-twitter.svg",
    },
    {
      link: "https://friday-template.webflow.io/landing/01#",
      image: "/assets/61e5bb75ba3a7e5fe50bd4a6_icon-linkedin.svg",
    },
    {
      link: "https://friday-template.webflow.io/landing/01#",
      image: "/assets/61e5bb75ba3a7ee2f50bd4a7_icon-youtube.svg",
    },
  ],
  companyName: "Friday",
  creatorCompany: "THC",
  creatorCompanyWebsite: "http://www.webflow.com/",
  creatorName: "JP",
  creatorLink: "https://webflow.com/templates/designers/jp",
});
</script>

<style></style>
