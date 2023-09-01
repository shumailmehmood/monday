<template>
  <div>
    <div v-if="simple">
      <div class="card gray">
        <div class="card-content">
          <div class="media">
            <div class="media-left">
              <figure class="image">
                <img
                  class="image"
                  src="https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/efficiency/efficiency_logo.png"
                  alt="Placeholder image"
                />
              </figure>
            </div>
          </div>

          <div class="content">
            <h1 class="extra-large">
              <b>Explore proven ways to work more efficiently</b>
            </h1>
            <Button text="Browse by use case" :normal="true" />
          </div>
        </div>
      </div>
    </div>
    <div v-else-if="award">
      <div class="card award-card">
        <div class="award-image">
          <img :src="award_Card_data.image" alt="" />
        </div>
        <div class="award-centent">
          <h1 class="title">{{ award_Card_data.title }}</h1>
          <h2 class="subtitle">
            {{ award_Card_data.subtitle }}
          </h2>
        </div>
      </div>
    </div>
    <div v-else>
      <div class="card is-flex is-flex-direction-column-reverse">
        <div class="image-main">
          <figure class="image">
            <img
              src="https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/efficiency/Simplify_OKR_tracking.png"
              alt="Placeholder image"
            />
          </figure>
        </div>
        <div class="card-content padding">
          <div class="content">
            <p class="text-small">Simplify OKR tracking</p>
            <div class="percentage is-flex is-align-items-center">
              <img
                src="https://dapulse-res.cloudinary.com/image/upload/v1672315351/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/efficiency/arrow_up.png"
                alt=""
              />
              <b class="extra-large blue">80%</b>
            </div>
            <h2 class="medium">of goals achieved with OKRs on monday.com</h2>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Button from "./Button.vue";

export default {
  name: "Cards-vue",
  props: {
    simple: Boolean,
    award: Boolean,
    award_Card_data: Object,
  },
  components: { Button },
};
</script>
<style scoped>
.image {
  max-height: 28px;
}
.text-small {
  font-size: 14px;
}
.extra-large {
  font-size: 2.75rem;
}
.blue {
  color: rgb(97, 97, 255);
}
.gray {
  background-color: rgb(236, 239, 248);
  padding: 40px 20px;
}
.image-main {
  border-bottom-left-radius: 10px;
  border-bottom-right-radius: 10px;
  overflow: hidden;
  height: 185px;
}
.image-main img {
  width: 100%;
  height: 185px;
}
.card {
  box-shadow: 0px 8px 24px 0 rgba(29, 140, 242, 0.16);
  border-radius: 10px;
  transition: all 0.5s ease;
  overflow: hidden;
}
.card:hover {
  cursor: pointer;
  box-shadow: 0px 8px 24px 0 rgba(29, 140, 242, 0.32);
}
.padding {
  padding: 40px;
}
.percentage img {
  height: 28px;
  width: 12px;
}
.medium {
  font-size: 1.125rem;
  font-weight: 400;
}
.percentage {
  gap: 0px 10px;
}
.award-card {
  width: 286px;
  z-index: 2;
  margin: 32px 10px 0;
  padding: 32px;
  border-radius: 8px;
  background-color: white;
  box-shadow: 0px 8px 24px 0 rgba(29, 140, 242, 0.16);
  transition: filter 0.2s ease-in-out;
  color: #333333;
  position: relative;
  .award-image {
    width: 100%;
    display: flex;
    justify-content: center;
  }
  .award-image img {
    max-height: 100px;
  }
  .title {
    font-size: 1.125rem;
    line-height: 24px;
    -webkit-letter-spacing: -0.5px;
    -moz-letter-spacing: -0.5px;
    -ms-letter-spacing: -0.5px;
    letter-spacing: -0.5px;
    font-weight: 500;
    margin-bottom: 24px;
    min-height: 64px;
    text-align: center;
    margin-top: 13px;
  }
  .subtitle {
    text-align: center;
    font-size: 1rem;
    line-height: 24px;
  }
}
</style>
