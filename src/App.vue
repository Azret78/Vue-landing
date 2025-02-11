<template>
  <the-header></the-header>
  <div class="wrapper">
    <main class="main">
      <app-index></app-index>
      <app-services></app-services>
      <app-standart></app-standart>
      <app-about></app-about>
      <app-faq></app-faq>
    </main>
  </div>
</template>

<script>
import TheHeader from "./components/global/TheHeader.vue";
import AppIndex from "./components/section/AppIndex.vue";
import AppServices from "./components/section/AppServices.vue";
import AppStandart from "./components/section/AppStandart.vue";
import AppAbout from "./components/section/AppAbout.vue";
import AppFaq from "./components/section/AppFaq.vue";

export default {
  components: {
    TheHeader,
    AppIndex,
    AppServices,
    AppStandart,
    AppAbout,
    AppFaq,
  },
};
</script>
