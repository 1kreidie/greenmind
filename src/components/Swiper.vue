<script>
    import { Swiper, SwiperSlide } from 'swiper/vue';
    import { Pagination, Navigation } from 'swiper/modules';
    import 'swiper/css';
    import 'swiper/css/pagination';
    import 'swiper/css/navigation';
    export default {
      components: {
        Swiper,
        SwiperSlide,
      },
      data() {
        return {
          modules: [Pagination, Navigation],
        };
      },
    };
</script>
  
<template>
  <swiper
      :slidesPerView="3"
      :spaceBetween="30"
      :loop="true"
      :pagination="{
        clickable: true,
      }"
      :navigation="true"
      :modules="modules"
      class="mySwiper"
    >
    <SwiperNavigation />
      <swiper-slide><img src="../assets/img/slide1.png" alt=""></swiper-slide>
      <swiper-slide><img src="../assets/img/slide2.png" alt=""></swiper-slide>
      <swiper-slide><img src="../assets/img/slide1.png" alt=""></swiper-slide>
      <swiper-slide><img src="../assets/img/slide3.png" alt=""></swiper-slide>
  </swiper>
</template>

  
<style lang="sass" scoped>
.swiper-slide
  & img 
    width: 373px
    height: 486px
  &-active img
    padding-right: 30px
    width: 404px
    height: 582px
</style>