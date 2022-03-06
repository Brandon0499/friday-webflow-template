<template>
  <div class="container">
    <div class="w-layout-grid main-grid">
      <div
        id="w-node-_6e7598f0-4ae8-b765-38bc-ef4f35557c1a-0e305478"
        class="center-wrapper inner-padding-medium"
      >
        <h2 class="heading-large margin-bottom-xsmall">
          <slot name="companySubInfoTitle"></slot>
        </h2>
        <p class="medium-paragraph">
          <slot name="companySubInfoParagraph"></slot>
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({});
</script>

<style></style>
