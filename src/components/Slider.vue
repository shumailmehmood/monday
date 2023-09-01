<template>
  <div>
    <div>
      <div class="box">
        <div class="absolute">
          <div class="name-and-job-description">
            <span class="quoteText"
              >monday.com has given me the confidence because when I walk into
              the room I know that when upper management asks for a certain
              piece of information I’m able to quickly provide it for
              them.”</span
            >
          </div>

          <div class="quote name-and-job-description">
            Kenny Wallace | Vendor Tooling Engineer, Nissan North America
          </div>

          <img
            src="https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/reviews/oscar_logo.svg"
            alt=""
          />
        </div>
      </div>
      <div class="imgbox is-flex is-justify-content-flex-end">
        <div class="circles is-flex">
          <div class="circle"></div>
          <div class="circle"></div>
          <div class="circle"></div>
          <div class="circle"></div>
          <div class="circle"></div>
        </div>
        <div class="img">
          <img
            src="https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/reviews/the_student_hotel_image.png"
            alt=""
          />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Slider-vue",
};
</script>
<style scoped>
.box {
  width: 540px;
  height: 320px;
  background-color: rgb(97, 97, 255);
  color: white;
  font-size: 20px;
  font-weight: 400;
  position: relative;
  padding: 27px 50px;
}
.quote {
  font-size: 14px;
  margin-top: 30px;
  margin-bottom: 10px;
}
.absolute {
  position: relative;
  top: 0px;
}
.circles {
  gap: 0px 10px;
}
.circle {
  width: 12px;
  height: 12px;
  background-color: white;
  border: 1px solid black;
  border-radius: 50%;
  transition: all 0.5s ease-in-out;
}
.blue {
  background-color: rgb(97, 97, 255);
}
.circle:hover {
  scale: 1.5;
  /* background-color: rgb(97, 97, 255); */
  /* border: none; */
  cursor: pointer;
}
.img {
  width: 200px;
  height: 200px;
  border-radius: 10px;
  overflow: hidden;
  position: relative;
  left: 60px;
  bottom: 80px;
}
.img img {
  width: 100%;
  height: 100%;
}
.imgbox {
  gap: 10px 20px;
}
</style>
