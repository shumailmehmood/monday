<template>
  <div>
    <div
      for="click"
      :class="[
        `boxi ${
          color == 'pink'
            ? 'pink'
            : color == 'purple'
            ? 'purple'
            : color == 'aqua'
            ? 'aqua'
            : color == 'dark-aqua'
            ? 'dark-aqua'
            : color == 'green'
            ? 'green'
            : color == 'blue'
            ? 'blue'
            : color == 'orange'
            ? 'orange'
            : color == 'yellow'
            ? 'yellow'
            : ''
        } `,
      ]"
      @click="check"
    >
      <input
        id="click"
        type="checkbox"
        :class="[
          `custom-checkbox ${
            color == 'pink'
              ? 'checkpink'
              : color == 'blue'
              ? 'checkblue'
              : color == 'green'
              ? 'checkgreen'
              : color == 'dark-aqua'
              ? 'checkdark-aqua'
              : color == 'purple'
              ? 'checkpurple'
              : color == 'orange'
              ? 'checkorange'
              : color == 'yellow'
              ? 'checkyellow'
              : color == 'aqua'
              ? 'checkaqua '
              : ' '
          } `,
        ]"
        v-model="checked"
      />

      <div class="img">
        <img :src="img" alt="" />
      </div>
      <p>{{ title }}</p>
    </div>
  </div>
</template>
<script>
export default {
  name: "checkbox-vue",
  props: {
    img: String,
    title: String,
    color: String,
  },
  data() {
    return {
      checked: false,
    };
  },
  methods: {
    check() {
      this.checked = !this.checked;
    },
  },
};
</script>
<style scoped>
.img {
  width: 35px;
  height: auto;
  margin: 0% auto;
}
.img img {
  width: 100%;
  height: 100%;
}
.boxi {
  margin: 0px 5px;
  width: 120px;
  height: 120px;
  /* padding: 20px 10px; */
  padding-left: 5px;
  padding-top: 5px;
  padding-bottom: 10px;
  padding-right: 5px;
  /* background-color: green; */
  border-radius: 8px;
  /* border: 1px solid rgb(255, 255, 255, 0.3); */
  border: 1px solid rgb(222, 222, 222);
}
p {
  text-align: center;
  font-weight: 300;
  font-size: 0.9rem;
}
.custom-checkbox {
  width: 20px;
  height: 20px;
  position: relative;
}
.checkgreen {
  background-color: rgb(0, 200, 117);
}
.green:hover {
  border-color: rgb(0, 200, 117);
}
.yellow:hover {
  border-color: rgb(255, 153, 0);
}
.checkaqua {
  background-color: rgb(0, 210, 210);
}
.checkpurple {
  background-color: rgb(171, 205, 253);
}
.purple:hover {
  border-color: rgb(171, 205, 253);
}
.checkorange {
  background-color: rgb(255, 117, 117);
}
.checkdark-aqua {
  background-color: rgb(86, 158, 195);
}
.checkblue {
  background-color: rgb(108, 108, 255);
}
.blue:hover {
  border-color: rgb(108, 108, 255);
}
.dark-aqua:hover {
  border-color: rgb(86, 158, 195);
}
.orange:hover {
  border-color: rgb(255, 117, 117);
}
.aqua:hover {
  border-color: rgb(0, 210, 210);
}
.checkyellow {
  background-color: rgb(255, 153, 0);
}
.pink:hover {
  border-color: rgb(255, 138, 196);
}
.boxi:hover {
  cursor: pointer;
}
/* .boxi-blue:hover{

} */
.custom-checkbox:checked {
  appearance: none;
  -webkit-appearance: none;
  /* Change background color when checked */
  border-radius: 4px;
}
.checkpink {
  background-color: rgb(255, 191, 201);
}
.custom-checkbox:checked::before {
  content: "\2713"; /* Checkmark character */
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 16px; /* Adjust font size for the checkmark */
  color: white; /* Checkmark color */
  display: block;
}
/* */
.boxi:hover {
  cursor: pointer;
}
</style>
