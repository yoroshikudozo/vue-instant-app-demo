<template>
  <nav class="swiper-pagination">
    <ul class="swiper-pagination-list">
      <li class="swiper-pagination-bullet">
        <button
          href="#"
          class="swiper-pagination-bullet-button"
          :class="{ 'is-active': activeIndex === 0 }"
          @click.prevent="toSlide(0)"
        >
          home
        </button>
      </li>
      <li class="swiper-pagination-bullet">
        <button
          href="#"
          class="swiper-pagination-bullet-button"
          :class="{ 'is-active': activeIndex === 1 }"
          @click.prevent="toSlide(1)"
        >
          fp
        </button>
      </li>
      <li class="swiper-pagination-bullet">
        <button
          href="#"
          class="swiper-pagination-bullet-button"
          :class="{ 'is-active': activeIndex === 2 }"
          @click.prevent="toSlide(2)"
        >
          to
        </button>
      </li>
      <li class="swiper-pagination-bullet">
        <button
          href="#"
          class="swiper-pagination-bullet-button"
          :class="{ 'is-active': activeIndex === 3 }"
          @click.prevent="toSlide(3)"
        >
          list
        </button>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "SwiperNav",
  props: {
    activeIndex: Number
  },
  methods: {
    toSlide(index) {
      this.$emit("toSlide", index);
    }
  }
};
</script>

<style scoped lang="scss">
.swiper-pagination {
  position: absolute;
  bottom: 0;
  backdrop-filter: blur(4px);
  background: rgba(255, 255, 255, 0.6);
  box-shadow: 0 0 6px rgba(0, 0, 0, 0.15);
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
  width: 25%;
  height: 64px;
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
.swiper-pagination-bullet-button {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  background: none;
  border: none;
  cursor: pointer;

  &:focus {
    outline: none;
  }

  &.is-active {
    font-weight: bold;
  }
}
</style>
