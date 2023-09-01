<template>
  <div>
    <div class="dropdown is-up">
      <div class="dropdown-trigger">
        <button
          class="is-flex is-align-items-center gap"
          @click="toggle"
          aria-controls="dropdown-menu7"
        >
          <span class="icon befor">
            <i class="fa-solid fa-globe"></i>
          </span>
          <span>English</span>
          <span :class="[`icon is-small ${isactive ? 'rotate' : ''} `]">
            <i class="fa-solid fa-chevron-down"></i>
          </span>
        </button>
      </div>
      <div
        :class="[`dropdown-menu ${isactive ? 'show' : 'hide'} `]"
        id="dropdown-menu7"
        role="menu"
      >
        <div class="dropdown-content">
          <div class="dropdown-item">
            <p>
              You can add the <code>is-up</code> modifier to have a dropdown
              menu that appears above the dropdown button.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Updropdown-vue",
  data() {
    return {
      isactive: false,
    };
  },
  methods: {
    toggle() {
      this.isactive = !this.isactive;
    },
  },
};
</script>
<style scoped>
.hide {
  display: none;
}
.show {
  display: block;
}
.rotate {
  transform: rotate(180deg);
}
.gap {
  gap: 0px 5px;
}
</style>
