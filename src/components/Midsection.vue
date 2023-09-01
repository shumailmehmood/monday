<template>
  <div>
    <section class="first">
      <div class="topimg is-flex is-justify-content-center">
        <img
          class="mondayimg"
          src="https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/products/monday_products_small.svg"
          alt=""
        />
      </div>
      <div class="toptext">
        <h1 class="large-text text-center">
          End-to-end products to run <br />
          the core of your business
        </h1>
        <p class="small-text text-center mt-3">
          Tailored products designed for every aspect of your teams' needs.
        </p>
      </div>
      <div
        class="crads is-flex is-justify-content-center is-flex-wrap-wrap mt-4"
      >
        <div v-for="items in cards" :key="items">
          <Card
            :img="items.img"
            :list="items.list"
            :text1="items.text1"
            :text2="items.text2"
            :color="items.color"
          />
        </div>
      </div>
    </section>
    <section class="second is-flex is-align-items-center">
      <div class="columns">
        <div class="column">
          <Cards :simple="true" />
        </div>
        <div class="column">
          <Cards />
        </div>
        <div class="column"><Cards /></div>
      </div>
    </section>
    <section class="third">
      <div class="slider">
        <div class="columns">
          <div class="column sliderleft">
            <h1 class="large-text">
              See how <br />
              our customers <br />
              drive impact
            </h1>
            <div class="buton">
              <LearnButton text="read more success stories" />
            </div>
          </div>
          <div class="column">
            <Slider />
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
<script>
import Card from "./Card.vue";
import Cards from "./Cards.vue";
import LearnButton from "./LearnButton.vue";
import Slider from "./Slider.vue";

export default {
  name: "Midle-section",
  components: { Card, Cards, LearnButton, Slider },
  data() {
    return {
      cards: [
        {
          img: "https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/WM_new_logo/wm_main_logo_1.png",
          text1: "For professionals and teams managing tasks & workflows",
          text2:
            "Manage tasks, projects, and processes to fuel collaboration and efficiency at scale.",
          color: "pruple",
          list: [
            "Project management",
            "Portfolio management",
            "Resource management",
            "Goals & strategy",
          ],
        },
        {
          img: "https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/products/crm_main_logo.png",
          text1: "For sales professionals and customer-facing teams",
          text2:
            "Track and manage all aspects of your sales cycle, customer data, and more in one place.",
          color: "aqua",
          list: [
            "Contact management",
            "Sales pipeline",
            "Post-sales management",
            "Lead management",
          ],
        },
        {
          img: "https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/Dev_new_logo_July23/dev_main_logo1.png",
          text1: "For product and development professionals and teams",
          text2:
            "Build agile workflows to drive impact across your product, design, and R&D teams.",
          color: "green",
          list: [
            " Roadmap planning",
            "Scrum & Kanban",
            "Bug tracking",
            "Sprint dashboards",
          ],
        },
      ],
    };
  },
};
</script>
<style scoped>
.topimg {
  margin: 25px 0px;
}
.slider {
  margin: 80px 0px;
}
.mondayimg {
  /* width: 20px; */
  width: auto;
  height: 40px;
}
.sliderleft {
  margin-top: 40px;
}
.large-text {
  font-size: 2.75rem;
  line-height: 60px;
  font-weight: 700;
  color: rgb(51, 51, 51);
}
.buton {
  margin-top: 30px;
}
.text-center {
  text-align: center;
}
.mt-2 {
  margin-top: 10px;
}
.mt-3 {
  margin-top: 15px;
}
.mt-4 {
  margin-top: 20px;
}
.small-text {
  font-size: 1.125rem;
  /* line-height: 32px; */
  color: rgb(51, 51, 51);
}
.crads {
  padding-bottom: 100px;
}
.second {
  min-height: 100vh;
  background-color: rgb(236, 239, 248);
  width: 100%;
  padding: 10px 40px;
}
.third {
  min-height: 100vh;
  width: 100%;
}
.slider {
  padding: 0px 96px;
}
</style>
