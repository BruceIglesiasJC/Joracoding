<template>

    <NavbarVue class="" ></NavbarVue>
    <div class=" h-screen">
      <swiper 
      class=" h-full"
      :direction="'vertical'"
      :modules="modules"
      :mousewheel="true"
      :slides-per-view="1"
      :space-between="0"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
      >
        <swiper-slide v-for="(item, index) in items" :key="index" class=" bg-slate-600 text-lg text-red-700 w-full    font-extrabold text-center">
          <h2 class=" mt-5">
            repeticion {{item}}
          </h2>
        </swiper-slide>
      </swiper>
    </div>


</template>

<script setup>
  import { Swiper, SwiperSlide } from 'swiper/vue';
  import { Mousewheel } from 'swiper';
  import 'swiper/css/bundle';
  import NavbarVue from './components/Navbar.vue';
  
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