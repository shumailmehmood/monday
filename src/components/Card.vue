<template>
  <div>
    <div class="card">
      <div class="card-content">
        <div class="media">
          <div class="media-left">
            <figure>
              <img class="image" :src="img" alt="Placeholder image" />
            </figure>
          </div>
        </div>

        <div class="content">
          <p>{{ text1 }}</p>
          <p>
            {{ text2 }}
          </p>
          <div
            :class="[
              `divider ${
                color == 'aqua'
                  ? 'aquagradient'
                  : color == 'green'
                  ? 'greengradient'
                  : 'purplegradient'
              } `,
            ]"
          ></div>
          <div class="list">
            <p>Top use cases:</p>
            <ul>
              <li v-for="(item, index) in list" :key="index">
                <span
                  :class="[
                    `${
                      color == 'aqua'
                        ? 'aqua'
                        : color == 'green'
                        ? 'green'
                        : 'purple'
                    }`,
                  ]"
                  ><i class="fa-solid fa-check"></i></span
                >{{ item }}
              </li>
            </ul>
            <div class="buton mt-2">
              <Button text="Get Started" :simple="true" />
            </div>
            <div class="learnbutton">
              <LearnButton color="black" text="Learn more" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Button from "./Button.vue";
import LearnButton from "./LearnButton.vue";
export default {
  name: "Cardvue-Vue",
  components: {
    Button,
    LearnButton,
  },
  props: {
    img: String,
    text1: String,
    text2: String,
    list: Array,
    color: String,
  },
};
</script>
<style scoped>
.buton {
  height: 40px;
}
.card {
  width: 286px;
  z-index: 2;
  margin: 32px 10px 0;
  margin-top: 32px;
  margin-right: 10px;
  margin-bottom: 0px;
  margin-left: 10px;
  padding: 32px 24px;
  border-radius: 8px;
  background-color: white;
  box-shadow: 0px 8px 24px 0 rgba(29, 140, 242, 0.16);
  transition: filter 0.2s ease-in-out;
  color: #333333;
  position: relative;
}
.mt-2 {
  margin-top: 25px !important ;
}
.aquagradient {
  border-image: linear-gradient(
    to right,
    rgb(0, 210, 210),
    rgba(0, 210, 210, 0)
  );
}
.greengradient {
  border-image: linear-gradient(
    to right,
    rgb(0, 200, 117),
    rgba(0, 200, 117, 0)
  );
}
.purplegradient {
  border-image: linear-gradient(
    to right,
    rgb(97, 97, 255),
    rgba(97, 97, 255, 0)
  );
}
.divider {
  box-sizing: content-box;
  border-width: 1px;
  border-style: solid;
  border-image-slice: 1;
  margin-bottom: 20px;
  margin-top: 32px;
}
ul {
  list-style: none;
  margin: 0px;
}
.purple {
  color: #6161ff;
}
.green {
  color: rgb(0, 200, 117);
}
.aqua {
  color: rgb(63, 222, 221);
}
ul li {
  display: flex;
  gap: 0px 10px;
}
.learnbutton {
  width: 100%;
  display: flex;
  margin: 20px 0px;
  justify-content: center;
  align-items: center;
}
.image {
  max-height: 51px;
}
.media {
  margin: 0;
}
.content {
  color: #676879;
  font-size: 0.8125rem;
}
.card-content {
  padding-bottom: 0%;
}
.card {
  padding-bottom: 10px;
}
.card:hover {
  box-shadow: 0px 8px 24px 0 rgba(29, 140, 242, 0.32);
}
</style>
