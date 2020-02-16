<template>
  <swiper :options="swiperOption" ref="swiper" @slideChange="slideChange">
    <swiper-slide data-history="home">I'm Slide 1</swiper-slide>
    <swiper-slide data-history="faspa">I'm Slide 2</swiper-slide>
    <swiper-slide data-history="takeout">I'm Slide 3</swiper-slide>
    <swiper-slide data-history="list">I'm Slide 4</swiper-slide>
    <div class="swiper-pagination" slot="pagination">
      <ul class="swiper-pagination-list">
        <li
          class="swiper-pagination-bullet"
          :class="{ 'is-active': activeIndex === 0 }"
          @click="toSlide(0)"
        >
          home
        </li>
        <li
          class="swiper-pagination-bullet"
          :class="{ 'is-active': activeIndex === 1 }"
          @click="toSlide(1)"
        >
          faspa
        </li>
        <li
          class="swiper-pagination-bullet"
          :class="{ 'is-active': activeIndex === 2 }"
          @click="toSlide(2)"
        >
          takeout
        </li>
        <li
          class="swiper-pagination-bullet"
          :class="{ 'is-active': activeIndex === 3 }"
          @click="toSlide(3)"
        >
          list
        </li>
      </ul>
    </div>
  </swiper>
</template>

<script>
import { swiper, swiperSlide } from "vue-awesome-swiper";
export default {
  name: "Swiper",
  components: {
    swiper,
    swiperSlide
  },
  data() {
    return {
      activeIndex: 0,
      swiperOption: {
        pagination: {
          el: ".swiper-pagination",
          type: "custom"
        },
        history: { key: "slide" },
        preloadImages: false,
        lazy: true,
        clickable: true
      }
    };
  },
  computed: {
    swiper() {
      return this.$refs.swiper.swiper;
    }
  },
  methods: {
    toSlide(index) {
      this.swiper.slideTo(index);
    },
    slideChange() {
      this.activeIndex = this.swiper.activeIndex;
    }
  }
};
</script>

<style scoped lang="scss">
.swiper-container {
  position: relative;
  height: 100%;
  background: white;
}
.swiper-slide {
  display: flex;
  align-items: center;
  justify-content: center;
}
.swiper-pagination {
  position: absolute;
  bottom: 0;
}
.swiper-pagination-list {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  margin: 0;
  padding: 0;
  border-top: 1px solid #ddd;
}
.swiper-pagination-bullet {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 25%;
  height: 63px;
  background: none;
  box-sizing: border-box;
  border-right: 1px solid #ddd;
  border-radius: 0;
  color: #2c3e50;
  opacity: 1;
}
.swiper-pagination-bullet:last-child {
  border-right: none;
}
.swiper-pagination-bullet.is-active {
  font-weight: bold;
}
</style>
