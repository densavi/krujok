<script>
import Fancybox from "@/plugins/Fancybox.vue";
import {Navigation} from 'swiper/modules';
import {Swiper, SwiperSlide} from 'swiper/vue';
import 'swiper/css';


export default {
  name: 'PhotoSlider',
  components: {Fancybox, Swiper, SwiperSlide},
  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper);
    };
    const onSlideChange = () => {
      console.log('slide change');
    };
    return {
      onSwiper,
      onSlideChange,
      modules: [Navigation],
    };
  },
}
</script>

<template>
  <Fancybox
      :options="{
        Carousel: {
          infinite: true,
        },
      }"
      class="photo-slider"
  >
    <swiper
        :modules="modules"
        :slides-per-view="3"
        :space-between="5"
        @swiper="onSwiper"
        navigation
        @slideChange="onSlideChange"
    >
      <swiper-slide>
        <a class="photo-slider__slide" data-fancybox="gallery" href="https://lipsum.app/id/60/1600x1200">
          <img src="https://lipsum.app/id/60/200x150" width="200" height="150"/>
        </a>
      </swiper-slide>
      <swiper-slide>
        <a class="photo-slider__slide" data-fancybox="gallery" href="https://lipsum.app/id/61/1600x1200">
          <img src="https://lipsum.app/id/61/200x150" width="200" height="150"/>
        </a>
      </swiper-slide>
      <swiper-slide>
        <a class="photo-slider__slide" data-fancybox="gallery" href="https://lipsum.app/id/62/1600x1200">
          <img src="https://lipsum.app/id/62/200x150" width="200" height="150"/>
        </a>
      </swiper-slide>
      <swiper-slide>
        <a class="photo-slider__slide" data-fancybox="gallery" href="https://lipsum.app/id/63/1600x1200">
          <img src="https://lipsum.app/id/63/200x150" width="200" height="150"/>
        </a>
      </swiper-slide>
      <swiper-slide>
        <a class="photo-slider__slide" data-fancybox="gallery" href="https://lipsum.app/id/64/1600x1200">
          <img src="https://lipsum.app/id/64/200x150" width="200" height="150"/>
        </a>
      </swiper-slide>
    </swiper>
  </Fancybox>
</template>

<style lang="scss">
  .photo-slider {
    margin-bottom: 20px;
    &__slide {
      display: flex;
      img {
        width: 100%;
        height: 77px;
        object-fit: cover;
        border-radius: 10px;
      }
    }

    .swiper-button-next,
    .swiper-button-prev {
      position: absolute;
      z-index: 2;
      top: 50%;
      width: 20px;
      height: 20px;
      margin-top: -10px;
      cursor: pointer;
      background-image: url('~@/assets/icons/slider-next.svg');
      background-size: cover;
    }
    .swiper-button-next {
      right: 5px;
    }
    .swiper-button-prev {
      left: 5px;
      transform: rotate(180deg);
    }
  }
  .swiper-button-disabled {
    display: none !important;
  }
</style>