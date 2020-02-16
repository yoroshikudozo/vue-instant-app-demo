<template>
  <swiper :options="swiperOption" ref="swiper" @slideChange="slideChange">
    <swiper-slide data-history="home"><home-content /></swiper-slide>
    <swiper-slide data-history="fp"><fp-content /></swiper-slide>
    <swiper-slide data-history="to"><to-content /></swiper-slide>
    <swiper-slide data-history="list"><list-content /></swiper-slide>
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
import FpContent from "@/components/FpContent";
import ToContent from "@/components/ToContent";
import ListContent from "@/components/ListContent";
import SwiperNav from "@/components/SwiperNav";

export default {
  name: "Swiper",
  components: {
    swiper,
    swiperSlide,
    SwiperNav,
    HomeContent,
    FpContent,
    ToContent,
    ListContent
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
