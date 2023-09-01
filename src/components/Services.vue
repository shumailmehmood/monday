<template>
  <div>
    <div class="columns service-mian">
      <div class="column">
        <div class="top">
          <img
            src="https://dapulse-res.cloudinary.com/image/upload/f_auto,q_auto/remote_mondaycom_static/img/monday-logo-x2.png"
            alt=""
          />
        </div>
        <ul>
          <li v-for="(i, index) in service[0]" :key="index">
            <a href="">{{ i }}</a>
          </li>
        </ul>
      </div>
      <div class="column">
        <div class="top">
          <h1>Features</h1>
        </div>
        <ul>
          <li v-for="(i, index) in service[1]" :key="index">
            <a href="">{{ i }}</a>
          </li>
        </ul>
      </div>
      <div class="column monday-products is-one-fifth">
        <div class="top">
          <h1 class="">Monday products</h1>
        </div>
        <div class="list">
          <ul>
            <li v-for="(i, index) in service[5][0]" :key="index">
              <a href="" class="is-flex is-align-items-center is-2"
                ><img :src="i.img" alt="" />
                {{ i.list }}
              </a>
            </li>
          </ul>
        </div>
        <div class="more">
          <h1 class="my-10">More by monday.com</h1>
          <ul>
            <li v-for="(i, index) in service[5][1]" :key="index">
              <a href="" class="is-flex is-align-items-center is-2"
                ><img :src="i.img" alt="" />
                {{ i.list }}
              </a>
            </li>
          </ul>
        </div>
      </div>
      <div class="column">
        <div class="top">
          <h1>Use cases</h1>
        </div>
        <ul>
          <li v-for="(i, index) in service[2]" :key="index">
            <a href="">{{ i }}</a>
          </li>
        </ul>
      </div>
      <div class="column">
        <div class="top">
          <h1>Company</h1>
        </div>
        <ul>
          <li v-for="(i, index) in service[3]" :key="index">
            <a href="">{{ i }}</a>
          </li>
        </ul>
      </div>
      <div class="column">
        <div class="top">
          <h1>Resourses</h1>
        </div>
        <ul>
          <li v-for="(i, index) in service[4]" :key="index">
            <a href="">{{ i }}</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "services-vue",
  data() {
    return {
      service: [
        [
          " Pricing",
          "Templates",
          "Contact us",
          "SMB",
          "Enterprise",
          "Non profi",
          "App markeet place",
          "24/7 support",
        ],
        [" Docs", "Automations", "Files", "Dashboards", "Kanban", "Gantt"],
        [
          "Marketing",
          "Project management",
          "Sales",
          "Developers",
          "HR",
          "IT",
          "Operations",
          "Construction",
        ],
        [
          "About us",
          "Careers - Were hiring!",
          "monday-U",
          "Press",
          "Customer stories",
          "Become a partner",
          "Sustainability & ESG",
          "Affiliates",
          "Digital Lift",
          "Investor relati",
        ],
        [
          " Help Center",
          "Community",
          "Blog",
          "Whats new",
          "monday spaces",
          "Webinars",
          "Startup for startup",
          "Global events",
          "App development",
          "Find a partner",
          "Compare",
        ],
        [
          [
            {
              img: "https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/WM_new_logo/Footer_wm_logo.png",
              list: "monday Worked mangement",
            },
            {
              img: "https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/footer/crm_icon_footer.png",
              list: "monday sales CRM",
            },
            {
              img: "https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/footer/dev_new_mobile_footer_logo.png",
              list: "monday dev",
            },
          ],
          [
            {
              img: "https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/footer/workcanvas_icon_footer.png",
              list: "workCanvas",
            },
            {
              img: "https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/footer/workforms_icon_footer.png",
              list: "WorkForm",
            },
          ],
        ],
      ],
    };
  },
};
</script>
<style scoped>
.service-mian {
  padding: 0px 40px;
  padding-left: 20px;
  padding-bottom: 57px;
  border-bottom: 0.5px solid;
}
a {
  text-decoration: none;
  font-size: 0.8125rem;
  color: inherit;
}
ul {
  display: flex;
  flex-direction: column;
  gap: 15px 0px;
}
a {
  transition: all 0.3s ease;
}
li a:hover {
  color: rgb(77, 77, 246);
}
.top:hover {
  cursor: pointer;
}
.top {
  height: 32px;
}
.my-10 {
  margin: 10px 0px;
}
.top img {
  height: 100%;
}
.monday-products {
  position: relative;
  right: 38px;
}

.monday-products ul li img {
  height: 18px;
}
.monday-products ul li a {
  gap: 0px 10px;
}
.more {
  margin: 10px 0px;
}
</style>
