<template>
  <swiper :options="swiperOption" ref="swiper" @slideChange="slideChange">
    <swiper-slide data-history="home"><home-content /></swiper-slide>
    <swiper-slide data-history="faspa">I'm Slide 2</swiper-slide>
    <swiper-slide data-history="takeout">I'm Slide 3</swiper-slide>
    <swiper-slide data-history="list">I'm Slide 4</swiper-slide>
    <swiper-nav
      :activeIndex="activeIndex"
      @toSlide="toSlide"
      slot="pagination"
    />
  </swiper>
</template>

<script>
import { swiper, swiperSlide } from "vue-awesome-swiper";
import HomeContent from "@/components/HomeContent";
import SwiperNav from "@/components/SwiperNav";

export default {
  name: "Swiper",
  components: {
    swiper,
    swiperSlide,
    HomeContent,
    SwiperNav
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
  overflow: auto;
}
</style>
