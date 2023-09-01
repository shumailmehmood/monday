<template>
  <div>
    <div class="tab">
      <div
        v-for="(items, index) in tabs"
        :key="index"
        @click="activateTab(index)"
        class="tab1 is-mobile-width-mobile width-desktop"
      >
        <img
          v-if="activetab === index"
          class="gray-image"
          :src="items.img2"
          alt=""
        />
        <img v-else :src="items.img" alt="" />
        <h2 :class="[`${activetab === index ? 'blue' : 'gray'}`]">
          {{ items.name }}
        </h2>
        <div :class="[`line ${activetab === index ? 'show' : ' none'} `]"></div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Tab-vue",
  data() {
    return {
      tabs: [
        {
          name: "Boards",
          img2: "https://dapulse-res.cloudinary.com/image/upload/e_colorize,co_rgb:6161FF/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/tabs/board_icon.svg",
          img: "https://dapulse-res.cloudinary.com/image/upload/e_colorize,co_rgb:0F1048/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/tabs/board_icon.svg",
          text: "Everything starts with a visual board — the core of monday.com Work OS. Tailor it your way and manage anything from projects to departments.",
        },
        {
          name: "Views",
          img: "https://dapulse-res.cloudinary.com/image/upload/e_colorize,co_rgb:0F1048/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/tabs/views_icon.svg",
          img2: "https://dapulse-res.cloudinary.com/image/upload/e_colorize,co_rgb:6161FF/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/tabs/views_icon.svg",
          text: "Visualize and plan your work more efficiently with multiple views: Kanban board, calendar, timeline, Gantt chart, and more",
        },
        {
          name: "Dashboard",
          img2: "https://dapulse-res.cloudinary.com/image/upload/e_colorize,co_rgb:6161FF/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/tabs/dashboard_icon.svg",
          img: "https://dapulse-res.cloudinary.com/image/upload/e_colorize,co_rgb:0F1048/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/tabs/dashboard_icon.svg",
          text: "Get the insights you need to make decisions with confidence. Keep track of progress, timelines, and budgets with custom dashboards.",
        },
        {
          name: "Intergrations",
          img: "https://dapulse-res.cloudinary.com/image/upload/e_colorize,co_rgb:0F1048/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/tabs/integrations_icon.svg",
          img2: "https://dapulse-res.cloudinary.com/image/upload/e_colorize,co_rgb:6161FF/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/tabs/integrations_icon.svg",
          text: "Connect monday.com with all your favorite tools and get more work done. Integrate Slack, Dropbox, Adobe Creative Cloud, and more.",
        },
        {
          name: "Automation",
          img2: "https://dapulse-res.cloudinary.com/image/upload/e_colorize,co_rgb:6161FF/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/tabs/automations_icon.svg",
          img: "https://dapulse-res.cloudinary.com/image/upload/e_colorize,co_rgb:0F1048/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/tabs/automations_icon.svg",
          text: "Streamline processes to focus on the work that matters. Choose from a variety of automation recipes or create your own in minutes.",
        },
        {
          name: "Apps",
          img: "https://dapulse-res.cloudinary.com/image/upload/e_colorize,co_rgb:0F1048/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/tabs/apps_icon.svg",
          img2: "https://dapulse-res.cloudinary.com/image/upload/e_colorize,co_rgb:6161FF/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/tabs/apps_icon.svg",
          text: "Expand the capabilities of your Work OS with monday apps. Enhance your workflows with custom views, widgets, integrations, and more.",
        },
        {
          name: "Docs",
          img: "https://dapulse-res.cloudinary.com/image/upload/e_colorize,co_rgb:0F1048/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/tabs/docs_icon.svg",
          img2: "https://dapulse-res.cloudinary.com/image/upload/e_colorize,co_rgb:6161FF/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/tabs/docs_icon.svg",
          text: "Transform text into action items, in just a few clicks. Connect, collaborate, and execute ideas and workflows in real-time from any doc.",
        },
      ],
      activetab: 0,
    };
  },
  created() {
    this.activateTab(this.activetab);
  },
  methods: {
    activateTab(index) {
      this.activetab = index;
      const data = this.tabs.filter((e, index) => {
        if (this.activetab === index) {
          return {
            e,
          };
        }
      });
      this.$emit("recivedata", data);
    },
  },
};
</script>
<style scoped>
.tab {
  height: 83px;
  box-shadow: 0px 10px 30px rgba(29, 140, 242, 0.2);
  border-radius: 8px;
  display: flex;
  justify-content: center;
  /* flex-wrap: wrap; */
  width: fit-content;
  box-sizing: border-box;
}
img {
  width: 16px;
}
.gray-img {
  /* filter: sepia(100%) invert(1) saturate(3) hue-rotate(226deg); */
  opacity: 0.6;
}
.gray {
  color: rgb(15, 16, 72);
}
h2 {
  font-weight: 300;
  opacity: 0.6;
  margin-top: 10px;
}
.width-desktop {
  width: 103px;
}
.tab1 {
  height: 100%;
  color: black;
  padding: 20px 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  font-size: 14px;
  position: relative;
}
.tab1:hover {
  background-color: #f0f3ff;
  cursor: pointer;
}
.width-mobile {
  width: 80px;
}
.line {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 4px;

  border-top-left-radius: 8px;
  border-top-right-radius: 8px;
  background-color: blue;
  transition: all 0.2s ease-in-out;
}
.none {
  opacity: 0;
}
.show {
  opacity: 1;
}
.blue {
  color: rgb(80, 52, 255);
  opacity: 1;
}
.colored-image {
  filter: sepia(300%) hue-rotate(150deg) saturate(450%);
}
</style>
