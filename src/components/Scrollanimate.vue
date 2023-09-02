<template>
  <div>
    <div class="main">
      <div class="scroll-controller">
        <div class="left">
          <div class="left-content-main left-content-main1">
            <div class="content">
              <div class="text">
                <h1><b>Streamline your work for maximum productivity</b></h1>
                <h2>
                  Centralize all your work, processes, tools, and files into one
                  Work OS. Connect teams, bridge silos, and maintain one source
                  of truth across your organization.
                </h2>
              </div>
              <div class="image-box">
                <div class="left-content">
                  <img
                    src="https://dapulse-res.cloudinary.com/image/upload/r_400/f_auto,q_auto/remote_mondaycom_static/uploads/BarBen/jane.jpeg"
                    alt=""
                  />
                </div>
                <p>
                  “ We use monday.com for a plethora of use cases, the
                  opportunities this platform provides are limitless.” <br />
                  <span>
                    <b>Jane Tham | VP of Collaboration Technologies</b>
                  </span>
                  <br />
                  Universal Music Group
                </p>
              </div>
            </div>
          </div>
          <div class="left-content-main left-content-main2">
            <div class="content">
              <div class="text">
                <h1><b>Streamline your work for maximum productivity</b></h1>
                <h2>
                  Centralize all your work, processes, tools, and files into one
                  Work OS. Connect teams, bridge silos, and maintain one source
                  of truth across your organization.
                </h2>
              </div>
              <div class="image-box">
                <div class="left-content">
                  <img
                    src="https://dapulse-res.cloudinary.com/image/upload/r_400/f_auto,q_auto/remote_mondaycom_static/uploads/BarBen/jane.jpeg"
                    alt=""
                  />
                </div>
                <p>
                  “ We use monday.com for a plethora of use cases, the
                  opportunities this platform provides are limitless.” <br />
                  <span>
                    <b>Jane Tham | VP of Collaboration Technologies</b>
                  </span>
                  <br />
                  Universal Music Group
                </p>
              </div>
            </div>
          </div>
          <div class="left-content-main last">
            <div class="content">
              <div class="text">
                <h1><b>Streamline your work for maximum productivity</b></h1>
                <h2>
                  Centralize all your work, processes, tools, and files into one
                  Work OS. Connect teams, bridge silos, and maintain one source
                  of truth across your organization.
                </h2>
              </div>
              <div class="image-box">
                <div class="left-content">
                  <img
                    src="https://dapulse-res.cloudinary.com/image/upload/r_400/f_auto,q_auto/remote_mondaycom_static/uploads/BarBen/jane.jpeg"
                    alt=""
                  />
                </div>
                <p>
                  “ We use monday.com for a plethora of use cases, the
                  opportunities this platform provides are limitless.” <br />
                  <span>
                    <b>Jane Tham | VP of Collaboration Technologies</b>
                  </span>
                  <br />
                  Universal Music Group
                </p>
              </div>
            </div>
          </div>
          <!-- <div class="cocntent1"></div>
          <div class="cocntent1 last"></div> -->
        </div>
        <div class="right">
          <div class="animated-images">
            <div class="scroll-image" id="scroll-image1">
              <div class="desktop shaddow">
                <div class="top">
                  <div class="circle"></div>
                  <div class="circle"></div>
                  <div class="circle"></div>
                </div>
                <div class="pic">
                  <video
                    preload="auto"
                    poster="https://dapulse-res.cloudinary.com/video/upload/so_0p/Generator_featured images/Home Page - 2022 Rebrand/parallax/goals_dashboard.jpg"
                    playsinline=""
                    webkit-playsinline=""
                    x5-playsinline=""
                    style="width: 100%; height: 100%"
                  >
                    <source
                      src="https://dapulse-res.cloudinary.com/video/upload/q_auto,f_auto,cs_copy/Generator_featured images/Home Page - 2022 Rebrand/parallax/goals_dashboard.mp4"
                    />
                  </video>
                </div>
              </div>
            </div>
            <div class="scroll-image image2">
              <div class="desktop shaddow">
                <img
                  src="https://colorlib.com/wp/wp-content/uploads/sites/2/glint-free-mobile-friendly-website-template.jpg.webp"
                  alt=""
                />
              </div>
            </div>
            <div class="scroll-image last-image">
              <div class="desktop shaddow">
                <div class="top">
                  <div class="circle"></div>
                  <div class="circle"></div>
                  <div class="circle"></div>
                </div>
                <div class="pic">
                  <video
                    preload="auto"
                    poster="https://dapulse-res.cloudinary.com/video/upload/so_0p/Generator_featured images/Home Page - 2022 Rebrand/parallax/goals_dashboard.jpg"
                    playsinline=""
                    webkit-playsinline=""
                    x5-playsinline=""
                    style="width: 100%; height: 100%"
                  >
                    <source
                      src="https://dapulse-res.cloudinary.com/video/upload/q_auto,f_auto,cs_copy/Generator_featured images/Home Page - 2022 Rebrand/parallax/goals_dashboard.mp4"
                    />
                  </video>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
export default {
  name: "Scroll-animation",

  data() {
    return {};
  },

  mounted() {
    gsap.registerPlugin(ScrollTrigger);
    // Create a GSAP timeline
    gsap.to(".left-content-main ", {
      scrollTrigger: {
        trigger: ".main",
        pin: true,
        start: "top top", // Start animation when the trigger element is 80% from the top
        end: "bottom bottom", // End animation when the trigger element is 20% from the bottom
        scrub: 1,
        // markers: true,
        endTrigger: ".last",
        // Add debug markers (remove in production)
      },
      // duration: 0.5,
      y: "-250%",
    });

    gsap.to(".image2", {
      scrollTrigger: {
        trigger: ".left-content-main1",
        start: "top top ", // Start animation when the trigger element is 80% from the top
        end: "bottom bottom", // End animation when the trigger element is 20% from the bottom
        scrub: 1,
        markers: true,
        // endTrigger: ".last",
        // Add debug markers (remove in production)
      },
      // duration: 0.5,
      zIndex: 2,
      x: "120%",
    });
    gsap.to(".last-image", {
      scrollTrigger: {
        trigger: ".left-content-main2",
        start: "top top ", // Start animation when the trigger element is 80% from the top
        end: "bottom bottom", // End animation when the trigger element is 20% from the bottom
        scrub: 1,
        // markers: true,
        // endTrigger: ".last",
        // Add debug markers (remove in production)
      },
      // duration: 0.5,
      zIndex: 3,
      x: "120%",
    });
  },

  methods: {},
};
</script>

<style scoped>
.main {
  width: 100%;
  min-height: 100vh;
  background-color: rgb(24, 27, 52);
  display: flex;
  justify-content: center;
  color: white;
}
#scroll-image1 {
  left: 5%;
}
.scroll-controller {
  width: 90%;
  height: 100vh;
  display: flex;
}
.desktop {
  width: inherit;
  height: inherit;
  border-radius: 10px;
  overflow: hidden;
}
.image2 {
  left: -100%;
}
.last-image {
  left: -100%;
}
.scroll-image1 {
  z-index: 1;
  left: 0%;
}
.scroll-image img {
  height: 100%;
  width: 100%;
  object-fit: cover;
}
.scroll-image {
  position: absolute;
  width: 35vw;
  height: 302px;
  /* height: auto; */
  overflow: hidden;
  border-radius: 10px;
}
.pic {
  background-color: rgb(254, 254, 254);
}
.shaddow {
  box-shadow: -10.8923px 14.523px 35.0973px rgba(29, 140, 242, 0.2);
}
.top {
  width: 100%;
  height: 13px;
  background-color: rgb(117, 130, 154);
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
  display: flex;
  gap: 0px 5px;
  align-items: center;
}
.circle {
  width: 6px;
  height: 6px;
  background-color: white;
  border-radius: 50%;
}
.circle:nth-child(1) {
  margin-left: 10px;
}
.left {
  /* border: 2px solid red; */
  height: 100vh;
  width: 50%;
  overflow: hidden;
  margin: 0px auto;
}
.scroll-controller .right {
  height: 100vh;
  width: 50%;
  display: flex;
  /* justify-content: center; */
  align-items: end;
}
.right .animated-images {
  width: 90%;
  height: 80vh;
  /* border: 2px solid green; */
  overflow: hidden;
  padding: 10px 10px;
  padding-right: 10px;
  position: relative;
}
.left-content-main {
  min-height: 100vh;
  width: 80%;
  /* border: 1px solid red; */
  display: flex;
  align-items: end;
  margin: 74px auto;
}
.content {
  display: flex;
  flex-direction: column;
  /* align-items: end; */
  /* justify-content: space-between; */
  gap: 200px 0px;
}
.image-box {
  display: flex;
  gap: 0px 20px;
}
.left-content {
  height: 80px;
  width: 130px;
  border-radius: 50px;
  overflow: hidden;
}
.image-box .left-content img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.left-content-main h2 {
  font-size: 1.125rem;
  margin: 10px 0px;
  color: white;
  font-weight: 300;
}
.left-content-main p {
  font-size: 0.875rem;
}

.content h1 {
  font-size: 2.25rem;
  color: white;
}
</style>
