<template>
  <div>
    <div v-if="color == 'black'" class="main-button">
      <button class="black">
        {{ text }} <span> <i class="fa-solid fa-arrow-right-long"></i> </span>
      </button>
    </div>
    <div v-else class="main-button">
      <button class="blue">
        {{ text }} <span> <i class="fa-solid fa-arrow-right-long"></i> </span>
      </button>
      <div class="underline"></div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Learn-button",
  props: {
    text: String,
    color: String,
  },
};
</script>
<style>
.main-button {
  width: fit-content;
}
.blue {
  color: #4d4df6;
}
.black {
  color: black;
}
.black:hover {
  color: black;
}
button {
  font-size: 14px;
  padding: 5px 0px;
  transition: all 0.5s ease-in-out;
  background-color: transparent;
  width: auto;
  background-color: transparent;
  border: none;
}
button:hover {
  color: #4d4df6;
  cursor: pointer;
}
span {
  transition: all 0.5s ease-in-out;
}

.underline {
  height: 0.6px;
  background-color: #4d4df6;
  opacity: 0.7;
  transition: 0.5s ease-in-out;
}
.main-button:hover .underline {
  opacity: 1;
}
.main-button:hover span {
  margin-left: 2px;
}
</style>
