<template>
  <div>
    <div v-if="gradient" :class="[`gradient bounce-animate `]">
      <button class="button">
        {{ text }} <span> <i class="fa-solid fa-arrow-right-long"></i></span>
      </button>
    </div>
    <div v-else-if="simple" class="">
      <button class="button simple">
        {{ text }} <span> <i class="fa-solid fa-arrow-right-long"></i></span>
      </button>
    </div>
    <div v-else>
      <button class="button normal">
        {{ text }} <span> <i class="fa-solid fa-arrow-right-long"></i></span>
      </button>
    </div>
  </div>
</template>
<script>
export default {
  name: "Button-vue",
  props: {
    text: String,
    gradient: Boolean,
    simple: Boolean,
    normal: Boolean,
  },
};
</script>
<style scoped>
:root {
  --pink: rgb(255, 138, 196);
  --drak-pink: rgb(240, 64, 149);
  --green: rgb(0, 200, 117);
  --orange: rgb(255, 153, 0);
  --aqua: rgb(0, 210, 210);
  --purple: rgb(171, 205, 253);
  --redish: rgb(255, 117, 117);
  --dark-aqua: rgb(86, 158, 195);
  --blue: rgb(108, 108, 255);
}
button {
  /* background-color: var(--dark-aqua); */
  background-color: #4d4df6;
  color: white;
  font-size: 0.875rem;
  padding: 20px 30px;
  border-radius: 50px;
  transition: all 0.5s ease-in-out;
  border: none;
}
.simple {
  background-color: transparent;
  border: 0.6px solid rgba(0, 0, 0, 0.9);
  color: black;
  padding: 9px 15px;
  width: 190px;
}
.button {
  transition: all 0.5s ease-in-out;
}
.simple:hover {
  color: black;
  background: transparent;
  border-width: 1.7px;
  border-color: black;
}
button:hover {
  color: white;
  background-color: #4d4df6;
}
button:hover span {
  transform: translateX(5px);
}
.bounce-animate {
  animation: bounce 0.6s ease-in-out;
}
button span {
  transition: all 0.5s ease-in-out;
  margin: 0px 5px;
}

@keyframes bounce {
  0% {
    scale: 1.2;
    /* transform: translateX(30px); */
  }
  100% {
    scale: 1;
    /* transform: translate(20px); */
  }
}
</style>
