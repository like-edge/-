<template>
    <swiper
      :modules="modules"
      :slides-per-view="auto"
      :space-between="20"
      :autoplay="{delay: 1000,stopOnLastSlide: false}"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
      class = "p"
    >
      <swiper-slide><img src="../pic/喜羊羊.jpg"></swiper-slide>
      <swiper-slide><img src="../pic/怪兽.jpg"></swiper-slide>
      <swiper-slide><img src="../pic/灰太狼.jpg"></swiper-slide>
      <swiper-slide><img src="../pic/奥特曼.jpg"></swiper-slide>
    </swiper>
  </template>
<script>
import { Swiper, SwiperSlide} from 'swiper/vue';
import { Autoplay } from 'swiper/modules';

import 'swiper/css';
import 'swiper/css/autoplay';
export default {
    components: {
    Swiper,
    SwiperSlide,
    },
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
        modules: [Autoplay],
    };
    },
};
</script>

<style>
.p
{
    width: 400px;
}
</style>