<template>
  <main>
    <div class="navbar-Top">
      <Navbar />
    </div>
    <div class="hero">
      <Hero />
    </div>
    <div class="midsection">
      <Midsection />
    </div>
    <div class="footer">
      <Footer />
    </div>
  </main>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";
import Midsection from "@/components/Midsection.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "HomeView",
  components: {
    Navbar,
    Hero,
    Midsection,
    Footer,
  },
};
</script>
<style scoped>
* {
  margin: 0%;
  padding: 0%;
}
.navbar-top {
  height: 72px;
  width: 100%;
}
.hero {
  width: 100%;
  min-height: 100vh;
  /* background-color: aqua; */
  position: relative;
  top: 72px;
  padding-bottom: 30px;
}
.midsection {
  width: 100%;
  min-height: 100vh;
  /* background-color: aqua; */
  position: relative;
  top: 72px;
  margin-top: 80px;
}
.footer {
  width: 100%;
  min-height: 100vh;
  /* background-color: aqua; */
  position: relative;
  top: 72px;
}
</style>
