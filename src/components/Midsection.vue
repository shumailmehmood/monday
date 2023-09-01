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
        <p class="midum-text text-center mt-3">
          Tailored products designed for every aspect of your teams' needs.
        </p>
      </div>
      <div
        class="crads is-flex is-justify-content-center is-flex-wrap-wrap mt-4"
      >
        <div v-for="items in card" :key="items">
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
    <section class="four">
      <div class="columns">
        <div class="column is-flex is-align-items-center is-two-fifths">
          <img
            src="https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/customer-support/support_globe.png"
            alt=""
          />
        </div>
        <div class="column content">
          <h1 class="large-text">
            Supporting your growth <br />
            every step of the way
          </h1>
          <h2 class="small-text">
            Our support superheroes are a click away to help you get the most
            out of monday.com, so you can focus on working without limits
          </h2>
          <div class="icons">
            <div class="columns">
              <div class="column is-flex">
                <img
                  src="https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/customer-support/phone.png"
                  alt=""
                />
                <div class="text">
                  <h1>24/7</h1>
                  <p class="small-text">support anytime, anywhere</p>
                </div>
              </div>
              <div class="column is-flex">
                <img
                  src="https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/customer-support/heart.png"
                  alt=""
                />
                <div class="text">
                  <h1>Voted #1</h1>
                  <p class="small-text">Most Loved by customers on G2</p>
                </div>
              </div>
              <div class="column is-flex">
                <img
                  src="https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/customer-support/fast.png"
                  alt=""
                />
                <div class="text">
                  <h1>2 hour</h1>
                  <p class="small-text">average response time</p>
                </div>
              </div>
            </div>
          </div>
          <div class="buttons is-flex">
            <Button text="Get in Touch" />
            <LearnButton text="Visit our spourt center" />
          </div>
        </div>
      </div>
    </section>
    <section class="award">
      <div class="stars">
        <img
          src="https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/review-cards/stars.png"
          alt=""
        />
      </div>
      <h1 class="midum-text margin-y-20 text-center">
        An award-winning platform. Loved by customers.
      </h1>
      <p class="small-text text-center">Based on 10,000+ customer reviews.</p>
      <div class="cards is-flex is-flex-wrap-wrap is-justify-content-center">
        <div class="card-item" v-for="(i, index) in awardCardData" :key="index">
          <Cards :award="true" :award_Card_data="i" />
        </div>
      </div>
    </section>
    <section class="last">
      <div class="main">
        <h1 class="large-text my-26 text-white">
          Deliver your best work with monday.com
        </h1>
        <h3 class="text-center small-text" id="text-gray">
          No credit card needed ✦ Unlimited time on Free plan
        </h3>
        <div class="award-buton text-center my-26">
          <Button text="Get started " />
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
import Button from "./Button.vue";

export default {
  name: "Midle-section",
  components: { Card, Cards, LearnButton, Button, Slider },
  data() {
    return {
      card: [
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
      awardCardData: [
        {
          image:
            "https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/review-cards/trust.png",
          title: "Voted best feature set, relationship and value",
          subtitle: "“This is the best no-code platform I've ever seen.”",
        },
        {
          image:
            "https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/review-cards/capterra.png",
          title: "Shortlisted in over 8 software categories",
          subtitle: "“The perfect organizer and team builder.”",
        },
        {
          image:
            "https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/review-cards/g2.png",
          title: "Market leader across 18 categories",
          subtitle: '"Flexible product with near endless possibilities."',
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
.text-white {
  color: rgb(255, 255, 255);
}
#text-gray {
  color: rgb(254, 254, 254);
  font-weight: 400;
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
  font-weight: 300;
}
.midum-text {
  font-size: 1.75rem;
  line-height: 40px;
  font-weight: 400;
  color: black;
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
.four {
  padding: 0px 60px;
  .buttons {
    gap: 0px 30px;
    align-items: baseline;
  }

  .icons img {
    max-height: 32px;
  }
  .icons {
    display: flex;
    margin: 50px 0px;
    margin-bottom: 60px;
  }
  .text h1 {
    font-size: 1.463rem;
    line-height: 26px;
    font-weight: 500;
  }
  .content {
    padding: 0px 60px;
    padding-right: 80px;
  }
}
.award {
  min-height: 100vh;
  width: 100%;
  margin: 20px 0px;
  padding: 60px 0px;

  .stars {
    display: flex;
    justify-content: center;
  }
  .margin-y-20 {
    margin: 20px 0px;
  }
}
.last {
  min-height: 70vh;
  width: 100%;
  background-color: rgb(24, 27, 52);
  display: flex;
  align-items: center;
  justify-content: center;

  .main h2 {
    width: fit-content;
  }
  .main h2 {
    align-items: center;
  }
  .my-26 {
    margin: 26px 0px;
  }
}
</style>
