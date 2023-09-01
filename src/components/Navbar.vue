<template>
  <nav>
    <div class="nav is-flex is-align-items-center">
      <div class="logo">
        <img
          src="https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/remote_mondaycom_static/img/monday-logo-x2.png"
          alt=""
        />
      </div>
      <div
        class="nav-items resp is-flex is-align-items-center is-justify-content-space-between"
      >
        <div class="left">
          <ul class="is-flex is-align-items-center gap-4">
            <li>
              Products <span><i class="fa-solid fa-chevron-down"></i></span>
            </li>
            <li>
              Platform <span><i class="fa-solid fa-chevron-down"></i></span>
            </li>
            <li>
              Resourses <span><i class="fa-solid fa-chevron-down"></i></span>
            </li>
            <li>
              Teams <span><i class="fa-solid fa-chevron-down"></i></span>
            </li>
          </ul>
        </div>
        <div class="right is-flex is-align-items-center">
          <ul class="is-flex is-align-items-center gap-4">
            <li>Pricing</li>
            <li>Contact sales</li>
            <li>Login</li>
          </ul>
          <Button :normal="true" text="Get Started" />
        </div>
      </div>
      <div class="resicon" @click="changeNav">
        <div v-if="!isactive" class="icon">
          <i class="fa-solid fa-bars"></i>
        </div>
        <div v-else class="cross">
          <i class="fa-solid fa-xmark"></i>
        </div>
      </div>
    </div>
    <div :class="[` show-res ${isactive ? 'show' : 'hide'}`]">
      <div class="navlink">
        <div v-for="items in Dropdown" :key="items" class="items">
          <Dropdown :data="items" />
        </div>
        <div v-for="items in Navlink" :key="items" class="items">
          <p>{{ items }}</p>
        </div>
        <div class="img">
          <img
            src="https://dapulse-res.cloudinary.com/image/upload/mobile_menu/Download_on_the_App_Store_Badge_US-UK_RGB_blk_092917_1.png"
            alt=""
          />
          <div class="gohome is-flex is-align-items-center">
            <img
              src="https://dapulse-res.cloudinary.com/image/upload/mobile_menu/Monday.png"
              alt=""
            />
            Go to homePage
            <span><i class="fa-solid fa-arrow-right-long"></i></span>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>
<script>
import Button from "./Button.vue";
import Dropdown from "./Dropdown.vue";
export default {
  name: "Navbar-vue",
  components: {
    Button,
    Dropdown,
  },
  data() {
    return {
      isactive: false,
      Dropdown: [
        {
          name: "Features",
          items: ["Dashbord", "Integrations", "Dev", "IT"],
        },

        {
          name: "Resourses",
          title: "Leran",
          items: ["blog", "about us ", "certificates", "Contact us"],
        },

        {
          name: "Products",
          title: "Tailored to your team need's",
          items: ["monday works manegment", "monday scales CRM", "Monday dev"],
        },

        {
          name: "Teams",
          title: "By Team",
          items: [
            "Marketing",
            " projects ",
            "sales",
            "Operation",
            " it ",
            "hr",
          ],
        },
      ],
      Navlink: ["pricing", "Login", "Contact Sales"],
    };
  },
  methods: {
    changeNav() {
      this.isactive = !this.isactive;
    },
  },
};
</script>
<style scoped>
nav {
  width: 100%;
}
.nav {
  height: 72px;
  width: 100%;
  padding: 0px 32px;
  position: fixed;
  top: 0%;
  transition: background-color 200ms ease;
  background-color: #ffffff;
  z-index: 3;
}
.logo {
  height: 48px;
  /* width: 192px; */
  margin-right: 13px;
}
.logo img {
  height: 100%;
  width: 100%;
}
.nav-items {
  width: 100%;
}
.right {
  gap: 0px 20px;
}
ul {
  gap: 0px 10px;
  font-size: 0.875rem;
  color: #535768;
}
ul li {
  padding: 6px 10px;
  border-radius: 10px;
  transition: all 0.5s ease;
}
ul li:hover {
  cursor: pointer;
  color: #5034ff;
  background-color: #f0f3ff;
}
.resicon {
  display: none;
}
.resicon:hover {
  cursor: pointer;
}
.show-res {
  width: 100%;
  min-height: 300px; /* Set your desired min-height */
  max-height: 122vh;
  height: 100vh;
  /* background-color: #5034ff; */
  background-color: white;
  padding: 0px 4%;
  position: fixed;
  top: 70px;
  overflow-y: auto;
  z-index: 2;
}
.items {
  /* border: 1px solid gray; */
  border-bottom: 0.5px solid #f1efef;
  width: 100%;
  padding: 17px 0px;
}
.items p {
  font-size: 1.125rem;
  font-weight: 300;
  /* padding: 17px 0px; */
}
.items p:hover {
  cursor: pointer;
}
.img {
  width: 168px;
  margin: 0px auto;
  padding: 30px 0px;
}
.img img {
  width: 100%;
  height: 100%;
}
.gohome img {
  width: 20px;
}
.gohome {
  /* margin: 30px auto; */
  margin-top: 10px;
  margin-bottom: 70px;
  gap: 0px 10px;
  font-weight: 300;
  width: max-content;
}
.gohome:hover {
  cursor: pointer;
}
.gohome span {
  transition: all 0.5s ease-in-out;
}
.gohome:hover span {
  transform: translateX(5px);
}
.show {
  display: block;
}
.hide {
  display: none;
}
@media screen and (max-width: 1200px) {
  .nav-items {
    display: none !important ;
  }
  .nav {
    width: 100%;
    justify-content: space-between;
  }
  .resicon {
    font-size: 20px;
    display: block;
  }
}
</style>
