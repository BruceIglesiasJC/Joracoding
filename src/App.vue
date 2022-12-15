<template>
  <!-- <section v-for="(item, index) in items" :key="index" class=" bg-slate-600 text-lg text-red-700 h-screen w-full font-extrabold text-center border-y-4">repeticion {{index}}</section> -->

  <swiper 
    class="h-screen"
    :direction="'vertical'"
    :modules="modules"
    :mousewheel="true"
    :slides-per-view="1"
    :space-between="0"
    @swiper="onSwiper"
    @slideChange="onSlideChange"
  >
    <swiper-slide v-for="(item, index) in items" :key="index" class=" bg-slate-600 text-lg text-red-700 h-screen w-full font-extrabold text-center border-y-4">
      repeticion {{index}}
    </swiper-slide>

  </swiper>
</template>

<script setup>
  import { Swiper, SwiperSlide } from 'swiper/vue';
  import { Mousewheel } from 'swiper';
   // Import Swiper styles
  import 'swiper/css/bundle';

    const modules = [Mousewheel]
    const onSwiper = (swiper) => {
      console.log(swiper);
    };
    const onSlideChange = () => {
      console.log('slide change');
    };


  const items = [
    1,2,3,4
  ]

</script>