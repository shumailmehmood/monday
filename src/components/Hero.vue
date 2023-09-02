<template>
  <div>
    <div>
      <div class="text">
        <h1>
          A Platform Built For a <br />
          new Way Of Working
        </h1>
        <h3 class="medium-text">
          What Would You like to manage with monday.com Work OS?
        </h3>
      </div>
      <div class="boxes is-flex is-justify-content-center">
        <div v-for="items in checkbox" :key="items">
          <Checkbox
            :img="items.img"
            :color="items.color"
            :title="items.title"
          />
        </div>
      </div>
      <div class="gradientbutton">
        <Button class="buton" text="Get Started" :gradient="true" />
        <h2>No credit card needed ✦ Unlimited time on Free plan</h2>
      </div>
    </div>
    <div class="image-section">
      <div class="img">
        <img
          src="https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/remote_mondaycom_static/uploads/NaamaGros/HP_tests/HP_asset_white_bg.png"
          alt=""
        />
      </div>
      <h1 class="text-center medium-text">
        Trusted by 180,000 + Customers Worldwide
      </h1>
      <div
        class="images is-flex is-justify-content-center is-flex-wrap-wrap is-align-items-center"
      >
        <div class="container">
          <picture>
            <img
              src="https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/remote_mondaycom_static/img/customers/logos-v2/HoltCat.png"
              alt=""
            />
          </picture>
        </div>
        <div class="container">
          <picture>
            <img
              src="https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/remote_mondaycom_static/img/customers/logos-v2/canva.png"
              alt=""
            />
          </picture>
        </div>
        <div class="container">
          <picture id="img3">
            <img
              src="https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/remote_mondaycom_static/img/customers/logos-v2/coca_cola.png"
              alt=""
            />
          </picture>
        </div>
        <div class="container">
          <picture id="img4">
            <img
              src="https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/remote_mondaycom_static/img/customers/logos-v2/oxy.png"
              alt=""
            />
          </picture>
        </div>
        <div class="container">
          <picture
            ><img
              src="https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/remote_mondaycom_static/img/customers/logos-v2/lionsgate.png"
              alt=""
          /></picture>
        </div>
        <div class="container">
          <picture id="img6">
            <img
              src="https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/remote_mondaycom_static/img/customers/logos-v2/carrefour.png"
              alt=""
          /></picture>
        </div>
        <div class="container">
          <picture id="img7">
            <img
              src="https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/remote_mondaycom_static/img/customers/logos-v2/bd.png"
              alt=""
            />
          </picture>
        </div>
        <div class="container">
          <picture>
            <img
              src="https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/remote_mondaycom_static/img/customers/logos-v2/glossier.png"
              alt=""
            />
          </picture>
        </div>
        <div class="container">
          <picture>
            <img
              src="https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/remote_mondaycom_static/img/customers/logos-v2/universal.png"
              alt=""
          /></picture>
        </div>
      </div>
      <div class="textsection columns">
        <div class="column">
          <h1 class="text-large bold">
            The Work OS that lets you <br />
            shape workflows, your way
          </h1>
        </div>
        <div class="column">
          <p class="small-text light">
            Boost your team’s alignment, efficiency, and productivity by
            customizing any workflow to fit your needs.
          </p>
          <Button text="Get Started" />
        </div>
      </div>
      <div class="imagegrid">
        <div class="columns is-mobile">
          <div class="column is-one-quarter">
            <div class="columns is-mobile is-mobile is-deaktop">
              <div class="column is-one-quarter-mobile">
                <div class="timeline-mian">
                  <div class="timeline shaddow">
                    <video
                    autoplay
                    muted
                      preload="auto"
                      poster="https://dapulse-res.cloudinary.com/image/fetch/f_auto,q_auto/https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/Masonry/final/Timeline_column.jpg"
                      playsinline=""
                      webkit-playsinline=""
                      x5-playsinline=""
                      style="width: 100%; height: 100%"
                    >
                      <source
                        src="https://dapulse-res.cloudinary.com/video/upload/q_auto,f_auto,cs_copy/Generator_featured images/Home Page - 2022 Rebrand/Masonry/final/Timeline_column.mp4"
                      />
                    </video>
                  </div>
                </div>
                <div class="file-main">
                  <div class="files shaddow">
                    <video
                    autoplay
                    muted
                      preload="auto"
                      poster="https://dapulse-res.cloudinary.com/image/fetch/f_auto,q_auto/https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/Masonry/final/Status_column.jpg"
                      playsinline=""
                      webkit-playsinline=""
                      x5-playsinline=""
                      style="width: 100%; height: 100%"
                    >
                      <source
                        src="https://dapulse-res.cloudinary.com/video/upload/q_auto,f_auto,cs_copy/Generator_featured images/Home Page - 2022 Rebrand/Masonry/final/Status_column.mp4"
                      />
                    </video>
                  </div>
                </div>
              </div>
              <div class="column is-one-quarter-mobile task-progress-main">
                <div class="task-progress shaddow">
                  <video
                    preload="auto"
                    poster="https://dapulse-res.cloudinary.com/image/fetch/f_auto,q_auto/https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/Masonry/final/Battery.jpg"
                    playsinline=""
                    webkit-playsinline=""
                    x5-playsinline=""
                    style="width: 100%; height: 100%"
                  >
                    <source
                      src="https://dapulse-res.cloudinary.com/video/upload/q_auto,f_auto,cs_copy/Generator_featured images/Home Page - 2022 Rebrand/Masonry/final/Battery.mp4"
                    />
                  </video>
                </div>
              </div>
              <div class="column is-hidden-tablet"></div>
            </div>
            <div>
              <div class="img2mainleft shaddow email">
                <video
                autoplay
                muted
                  preload="auto"
                  poster="https://dapulse-res.cloudinary.com/image/fetch/f_auto,q_auto/https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/Masonry/final/Integration.jpg"
                  playsinline=""
                  webkit-playsinline=""
                  x5-playsinline=""
                  style="width: 100%; height: 100%"
                >
                  <source
                    src="https://dapulse-res.cloudinary.com/video/upload/q_auto,f_auto,cs_copy/Generator_featured images/Home Page - 2022 Rebrand/Masonry/final/Integration.mp4"
                  />
                </video>
              </div>
            </div>
            <div>
              <div
                class="img3mainleft pie-main is-hidden-mobile is-hidden-tablet-only"
              >
                <div class="pie-weight shaddow">
                  <video
                     autoplay
                     muted
                    preload="auto"
                    poster="https://dapulse-res.cloudinary.com/image/fetch/f_auto,q_auto/https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/Masonry/final/Pie.jpg"
                    playsinline=""
                    webkit-playsinline=""
                    x5-playsinline=""
                    style="width: 100%; height: 100%"
                    
                  >
                    <source
                      src="https://dapulse-res.cloudinary.com/video/upload/q_auto,f_auto,cs_copy/Generator_featured images/Home Page - 2022 Rebrand/Masonry/final/Pie.mp4"
                    />
                  </video>
                </div>
              </div>
            </div>
          </div>
          <div class="column mobile-main is-mobile-three-fifths is-one-fifth">
            <div class="mobile shaddow">
              <video
              autoplay
              muted
                preload="auto"
                poster="https://dapulse-res.cloudinary.com/image/fetch/f_auto,q_auto/https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/Masonry/final/MobileApp.jpg"
                playsinline=""
                webkit-playsinline=""
                x5-playsinline=""
                style="width: 100%; height: 100%"
              >
                <source
                  src="https://dapulse-res.cloudinary.com/video/upload/q_auto,f_auto,cs_copy/Generator_featured images/Home Page - 2022 Rebrand/Masonry/final/MobileApp.mp4"
                />
              </video>
            </div>
          </div>
          <div class="column">
            <div class="columns is-mobile">
              <div class="column is-one-quarter plus-mian">
                <div class="plus shaddow">
                  <video
                  autoplay
                  muted
                    preload="auto"
                    poster="https://dapulse-res.cloudinary.com/image/fetch/f_auto,q_auto/https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/Masonry/final/Automation.jpg"
                    playsinline=""
                    webkit-playsinline=""
                    x5-playsinline=""
                    style="width: 100%; height: 100%"
                  >
                    <source
                      src="https://dapulse-res.cloudinary.com/video/upload/q_auto,f_auto,cs_copy/Generator_featured images/Home Page - 2022 Rebrand/Masonry/final/Automation.mp4"
                    />
                  </video>
                </div>
              </div>
              <div class="column is-one-quarter profile-mian">
                <div class="profile shaddow">
                  <video
                  autoplay
                  muted
                    preload="auto"
                    poster="https://dapulse-res.cloudinary.com/image/fetch/f_auto,q_auto/https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/Masonry/final/Talk.jpg"
                    playsinline=""
                    webkit-playsinline=""
                    x5-playsinline=""
                    style="width: 100%; height: 100%"
                  >
                    <source
                      src="https://dapulse-res.cloudinary.com/video/upload/q_auto,f_auto,cs_copy/Generator_featured images/Home Page - 2022 Rebrand/Masonry/final/Talk.mp4"
                    />
                  </video>
                </div>
                <div class="column"></div>
              </div>
            </div>
            <div
              class="dashbord-main shaddow is-hidden-mobile is-hidden-tablet-only"
            >
              <div class="dashbord">
                <div class="top">
                  <div class="circle"></div>
                  <div class="circle"></div>
                  <div class="circle"></div>
                </div>
                <div class="pic">
                  <video 
                  autoplay
                  muted
                    preload="auto"
                    poster="https://dapulse-res.cloudinary.com/image/fetch/f_auto,q_auto/https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/Masonry/final/Dash.jpg"
                    playsinline=""
                    webkit-playsinline=""
                    x5-playsinline=""
                    style="width: 100%; height: 100%"
                  >
                    <source
                      src="https://dapulse-res.cloudinary.com/video/upload/q_auto,f_auto,cs_copy/Generator_featured images/Home Page - 2022 Rebrand/Masonry/final/Dash.mp4"
                    />
                  </video>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="scroll">
      <Scroll />
    </div>
    <div class="barsection">
      <div class="bartext">
        <h1 class="extra-large bold text-center">
          Everything you need for any workflow
        </h1>
        <p class="text-center medium-text">
          Easily build your ideal workflow with monday.com building blocks.
        </p>
      </div>
      <div class="tab is-flex is-justify-content-center">
        <Tab @recivedata="getdata" />
      </div>
      <div class="tabchange columns">
        <div class="column">
          <div class="video shaddow">
            <div class="top top-up">
              <div class="circle"></div>
              <div class="circle"></div>
              <div class="circle"></div>
            </div>
            <video
              preload="auto"
              loop=""
              poster="https://dapulse-res.cloudinary.com/video/upload/so_0p/Generator_featured images/Home Page - 2022 Rebrand/tabs/final-videos-tabs/7_status.jpg"
              playsinline=""
              webkit-playsinline=""
              x5-playsinline=""
              autoplay
              muted
              style="width: 100%; height: 100%"
            >
              <source
                src="https://dapulse-res.cloudinary.com/video/upload/q_auto,f_auto,cs_copy/Generator_featured images/Home Page - 2022 Rebrand/tabs/final-videos-tabs/7_status.mp4"
              />
            </video>
          </div>
        </div>
        <div class="column is-flex is-align-items-center">
          <div class="change-container">
            <div class="is-flex is-align-items-center">
              <img class="change-image is-3" :src="img" alt="" />
              <h2>{{ name }}</h2>
            </div>
            <p>
              {{ text }}
            </p>
            <div class="learn-button">
              <LearnButton text="Learn more" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
// import Button from "./Button.vue";
import Button from "./Button.vue";
import Tab from "./Tab.vue";
import Scroll from "./Scrollanimate.vue";
import Checkbox from "./Checkbox.vue";
import LearnButton from "./LearnButton.vue";
export default {
  name: "her-vue",
  components: {
    Checkbox,
    Button,
    Scroll,
    Tab,
    LearnButton,
  },
  data() {
    return {
      checkbox: [
        {
          color: "pink",
          title: "Creative & design",
          img: "https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/first_fold/icons/design_icon.png",
        },
        {
          color: "green",
          title: "Softwere development",
          img: "https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/first_fold/icons/dev_icon.png",
        },
        {
          color: "pink",
          title: "Marketing",
          img: "https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/first_fold/icons/marketing_icon.png",
        },
        {
          color: "yellow",
          title: "Project Management",
          img: "https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/first_fold/icons/pmo_icon.png",
        },
        {
          color: "aqua",
          title: "Sales & CRM",
          img: "https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/first_fold/icons/crm_icon.png",
        },
        {
          color: "purple",
          title: "Task Management",
          img: "https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/first_fold/icons/task_icon.png",
        },
        {
          color: "orange",
          title: "HR",
          img: "https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/first_fold/icons/hr_icon.png",
        },

        {
          color: "dark-aqua",
          title: "Operations",
          img: "https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/first_fold/icons/operations_icon.png",
        },
        {
          color: "blue",
          title: "More Workflows",
          img: "https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/first_fold/icons/workflows_icon.png",
        },
      ],
      img: "",
      text: "",
      name: "",
    };
  },
  methods: {
    getdata(data) {
      // console.log(data[0].name);
      this.img = data[0].img2;
      this.text = data[0].text;
      this.name = data[0].name;
    },
  },
};
</script>
<style scoped>
.text {
  /* padding: 20px 10%; */
  text-align: center;
  padding-top: 70px;
  color: rgb(59, 59, 59);
}
.text h1 {
  font-size: 4.5rem;
  font-weight: bold;
  line-height: 85px;
  word-break: break-all;
  margin-bottom: 2rem;
  /* font-family: ; */
}

.img {
  width: 100%;
  margin-bottom: 70px;
  height: 380px;
}
.img img {
  height: 100%;
  width: 100%;
  object-fit: cover;
}

.text-center {
  text-align: center;
}
.medium-text {
  font-size: 1.5rem;
}
.boxes {
  padding: 0 20px;
  padding-top: 3rem;
  padding-bottom: 2rem;
}
.images {
  /* gap: 0px 10px; */
  width: 100%;
  padding: 0px 50px !important ;
  margin: 30px 0px;
  gap: 20px 10px;
}
.light {
  font-weight: 300;
}
.small-text {
  font-size: 1.4rem;
}
#img4 {
  width: 58px;
  height: 56px;
}
#img6 {
  width: 70px;
  height: 56px;
}
.images .container {
  max-width: 100px;
  display: flex;
  align-items: center;
  justify-content: center;
  /* height: 108px; */
  height: auto;
  display: flex;
  overflow: hidden;
}
#img3 {
  width: 96px;
  height: 52px;
}
.bold {
  font-weight: bold;
}
.textsection h1 {
  color: black;
}
.text-large {
  font-size: 2rem;
}
#img7 {
  width: 96px;
  height: 45px;
}
.images .container picture {
  width: 96px;
  height: 26px;
}
.gradientbutton {
  text-align: center;
  /* margin: 50px 0px; */
  margin-top: 20px;
  margin-bottom: 60px;
}
.gradientbutton .buton {
  margin: 10px auto;
  width: fit-content;
}
.textsection {
  padding: 0px 30px;
  padding-top: 100px;
  padding-bottom: 30px;
}
.textsection .column h1 {
  text-transform: capitalize;
}
.textsection p {
  margin: 10px 0px;
  margin-bottom: 30px;
}
.imagegrid {
  padding: 30px 10px;
}
.timeline {
  background-color: white;
  /* border: 1px solid; */
  border-radius: 10px;
  overflow: hidden;
  width: 147px;
  /* margin: 10px 0px; */
}
.task-progress {
  width: 140px;
  /* border: 1px solid; */
  border-radius: 10px;
  height: 140px;
}
.email {
  width: 100%;
  height: 70px;
  /* border: 1px solid; */
  border-radius: 10px;
  /* background-color: aqua; */
  display: flex;
  justify-content: flex-start;
  background-color: white;
}
.pie-main {
  width: 100%;
  display: flex;
  justify-content: end;
}
.pie-weight {
  width: 150px;
  margin-top: 10px;
  height: 150px;
  /* border: 1px solid; */
  border-radius: 10px;
  background-color: white;
}
.mobile-mian {
  width: 178px;
  margin: 0%;
}
.mobile {
  padding: 10px;
  background: aliceblue;
  border-radius: 21px;
  width: 195px;
  margin: 0px auto;
}
.profile {
  padding: 10px;
  /* border: 1px solid; */
  border-radius: 10px;
  background-color: white;
}
.plus {
  padding: 10px;
  /* border: 1px solid; */
  border-radius: 10px;
  background-color: white;
}
.top {
  width: 100%;
  height: 15px;
  background-color: rgb(229, 242, 254);
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  gap: 0px 10px;
}
.dashbord {
  /* border: 1px solid; */
  border-radius: 10px;
}
.circle {
  width: 7px;
  height: 7px;
  background-color: white;
  border-radius: 50%;
}
.circle:nth-child(1) {
  margin-left: 15px;
}
.file-main {
  margin: 10px 0px;
  border-radius: 10px;
  width: 147px;
}
.files {
  width: 147px;
  border-radius: 10px;
  overflow: hidden;
}
.shaddow {
  box-shadow: -10.8923px 14.523px 35.0973px rgba(29, 140, 242, 0.2);
}
.extra-large {
  font-size: 3rem;
  color: black;
}
.bartext {
  /* padding: 50px 0px; */
  padding-top: 100px;
  padding-bottom: 30px;
}
.tab {
  margin: 40px 0px;
}
.tabchange {
  padding: 0px 100px;
}
.tabchange .video {
  width: 546px;
  height: 368px;
  padding: 15px 0px;
  /* background-color: black; */
  background-color: white;
  border-radius: 10px;
  overflow: hidden;
}
.top-up {
  position: relative;
  top: -15px;
}
.change-image {
  width: 24px;
  height: 24px;
}
.change-container {
  padding-left: 60px;
}
.change-container h2 {
  font-size: 1.75rem;
  line-height: 40px;
  font-weight: 400;
  color: rgb(97, 97, 255);
  text-transform: capitalize;
  margin: 0px 10px;
}
.change-container p {
  font-size: 1.125rem;
  line-height: 32px;
  font-weight: 400;
}
.learn-button {
  margin: 20px 0px;
}
@media screen and (max-width: 1200px) {
  .boxes {
    flex-wrap: wrap;
    gap: 20px 0px;
  }
}
</style>
