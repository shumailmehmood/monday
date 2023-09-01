<template>
  <div>
    <div class="dropdown">
      <div class="dropdown-trigger">
        <p
          :class="[`drop ${isactive ? 'common-color' : ''} `]"
          aria-haspopup="true"
          aria-controls="dropdown-menu3"
          @click="change"
        >
          <span>{{ data.name }}</span>
          <span :class="[`icon  transition ${isactive ? 'rotate' : ''} `]">
            <i class="fa-solid fa-chevron-down"></i>
          </span>
        </p>
      </div>
      <div
        :class="[`dropdown-menu ${isactive ? 'show' : 'none'} `]"
        id="dropdown-menu3"
      >
        <div class="dropdown-content">
          <div v-if="data.title" class="text dropdown-item">
            <span>
              {{ data.title }}
            </span>
            <hr class="dropdown-divider" />
          </div>
          <a
            href="#"
            v-for="items in data.items"
            :key="items"
            class="dropdown-item"
          >
            {{ items }}
          </a>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Dropdown-vue",
  props: {
    data: Object,
  },
  data() {
    return {
      isactive: false,
      items: null,
    };
  },
  created() {},
  methods: {
    change() {
      this.isactive = !this.isactive;
      console.log("oye");
    },
  },
};
</script>
<style scoped>
.show {
  display: block;
}
.none {
  display: none;
}
.dropdown {
  display: block;
}
p {
  font-size: 1.125rem;
  font-weight: 300;
}
p span:nth-child(2) {
  font-size: 0.8rem;
}
p:hover {
  cursor: pointer;
}
.rotate {
  transform: rotate(180deg);
}
.dropdown-item:hover {
  background: none;
}
.common-color {
  color: #595ad4;
}
.transition {
  transition: all 0.5s ease-in-out;
}
.dropdown-content {
  transition: all 0.5s ease-in-out;
  background-color: transparent;
  box-shadow: none;
}
.dropdown-menu {
  position: relative;
}
</style>
