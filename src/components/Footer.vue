<template>
  <footer class="section wf-section">
    <div class="container footer w-container">
      <div class="w-layout-grid main-grid footer">
        <div
          id="w-node-_2bca43ef-7cde-b5da-b1b2-716107bf8e46-07bf8e43"
          class="content-wrapper"
        >
          <img :src="companyLogo" loading="lazy" alt="" class="logo-footer" />
          <p class="main-paragraph">
            {{ companyDescription }}
          </p>
        </div>
        <ul
          role="list"
          class="w-list-unstyled"
          v-for="list in footerLists"
          :key="list"
        >
          <li>
            <h4 class="heading-small text-gray">
              {{ list.footerListName }}
            </h4>
          </li>

          <li v-for="sublist in list.footerSubLists" :key="sublist">
            <a :href="sublist.sublistLink" class="link-footer">{{
              sublist.footerSubListName
            }}</a>
          </li>
        </ul>

        <div
          id="w-node-_0bae9e82-9b29-b0df-f69c-0f24674e559d-07bf8e43"
          class="social-wrapper"
        >
          <a
            :href="socialMediaLink.link"
            class="link-icons center w-inline-block"
            v-for="socialMediaLink in socialMediaLinks"
            :key="socialMediaLink.image"
            ><img
              :src="socialMediaLink.image"
              loading="lazy"
              alt=""
              class="icon-social"
          /></a>
        </div>
        <div
          id="w-node-d6133a47-301a-a6de-46fb-2533b7c7a68a-07bf8e43"
          class="footer-inner"
        >
          <div class="main-paragraph size-small">
            © {{ companyName }} — Powered by
            <a :href="creatorCompanyWebsite" target="_blank">{{
              creatorCompany
            }}</a>
          </div>
        </div>
        <div
          id="w-node-_2bca43ef-7cde-b5da-b1b2-716107bf8e80-07bf8e43"
          class="footer-inner"
        >
          <div class="main-paragraph size-small">
            Created by
            <a :href="creatorLink" target="_blank">{{ creatorName }}</a>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
const props = defineProps({
  companyLogo: {
    type: String,
    required: true,
  },
  companyDescription: {
    type: String,
    required: true,
  },
  footerLists: {
    type: Array,
    required: true,
  },
  socialMediaLinks: {
    type: Array,
  },
  companyName: {
    type: String,
  },
  creatorCompany: {
    type: String,
  },
  creatorCompanyWebsite: {
    type: String,
  },
  creatorName: {
    type: String,
  },
  creatorLink: {
    type: String,
  },
});

// console.log(props.footerLists);
</script>

<style></style>
