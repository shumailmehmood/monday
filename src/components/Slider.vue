<template>
  <div>
    <div>
      <div class="box">
        <div class="absolute">
          <div class="name-and-job-description">
            <span class="quoteText">{{ quote }}</span>
          </div>

          <div class="quote name-and-job-description">
            {{ discription }}
          </div>

          <img :src="text_image" alt="" />
        </div>
      </div>
      <div class="imgbox is-flex is-justify-content-flex-end">
        <div class="circles is-flex">
          <div
            :class="[`circle ${activeCircle === index ? 'blue' : ''} `]"
            v-for="(i, index) in data"
            :key="index"
            @click="load(index, i)"
          ></div>
        </div>
        <div class="img">
          <img :src="figure" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Slider-vue",
  data() {
    return {
      activeCircle: 0,
      data: [
        {
          textimg:
            "https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/reviews/oscar_logo.svg",
          figure:
            "https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/reviews/oscar_image.png",
          qoute:
            "“Now that we have monday.com Work OS as the backbone of our organization I feel that I have an overview I can trust.”",
          discription: "Charlie MacGregor | Founder & CEO",
        },
        {
          textimg:
            "https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/reviews/telefonica_logo.svg",
          figure:
            "https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/reviews/the_student_hotel_image.png",
          qoute:
            "“With monday.com, we’re 30% more efficient at delivering hundreds of campaigns seen by millions of customers.”",
          discription: "Tye Rapley-Hawkins | Head of Delivery",
        },
        {
          textimg:
            "https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/reviews/zippo.svg",
          figure:
            "https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/reviews/zippo_image.png",
          qoute:
            "“monday.com Work OS has enabled our group to launch more product categories and expand into more markets in way less time.”",
          discription: "Chris Funk | Director of Product Innovation",
        },
        {
          textimg: "",
          figure:
            "https://dapulse-res.cloudinary.com/image/upload/Generator_featured%20images/Home%20Page%20-%202022%20Rebrand/reviews/nissan_image.png",
          qoute:
            "monday.com has given me the confidence because when I walk into the room I know that when upper management asks for a certain piece of information I’m able to quickly provide it for them.”",
          discription:
            "Kenny Wallace | Vendor Tooling Engineer, Nissan North America",
        },
      ],
      text_image: "",
      figure: "",
      quote: "",
      discription: "",
    };
  },
  async created() {
    await this.load(this.activeCircle);
  },
  methods: {
    load(index) {
      this.activeCircle = index;
      let res = this.data.map((e, i) => {
        if (this.activeCircle === i) {
          return e;
        } else {
          return;
        }
      });
      this.text_image = res[this.activeCircle].textimg;
      this.figure = res[this.activeCircle].figure;
      this.discription = res[this.activeCircle].discription;
      this.quote = res[this.activeCircle].qoute;
      console.log(index, "data is here", res);
    },
  },
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
  top: 32px;
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
  border: none;
  transition: all 0.5s;
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
