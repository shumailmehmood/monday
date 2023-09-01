<template>
  <div>
    <div class="secrvices">
      <Services />
    </div>
    <div class="faq">
      <Faq />
    </div>
  </div>
</template>

<script>
import Faq from "./Faq.vue";
import Services from "./Services.vue";

export default {
  name: "Footer-vue",
  components: { Services, Faq },
};
</script>

<style scoped>
.faq {
  width: 100%;
  margin-top: 20px;
}
</style>
