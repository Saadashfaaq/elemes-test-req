<template>
  <div class="hello">
    INI LANDING
  </div>

  <HeaderComp />
  <ContentComp />
  <FooterComp />
</template>

<script>
import HeaderComp from "../header/header.vue";
import ContentComp from "../content/content.vue";
import FooterComp from "../footer/footer.vue";

export default {
  name: "landingPage",
  props: {
    msg: String
  },
  components: {
    HeaderComp,
    ContentComp,
    FooterComp
  }
};
</script>
