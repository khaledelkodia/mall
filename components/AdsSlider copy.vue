<template>
  <div class="slider-ads-content">
    <button class="nav-btn prev-btn" @click="swiperRef?.slideNext()">
      <i class="fa-solid fa-caret-left"></i>
    </button>
    
    <swiper
      :modules="[SwiperAutoplay, SwiperPagination]"
      :slides-per-view="1"
      :loop="true"
      :autoplay="{
        delay: 3000,
        disableOnInteraction: false,
      }"
      :pagination="{ clickable: true }"
      class="mySwiper"
      @swiper="onSwiper"
    >
      <swiper-slide>
        <img src="/images/banners/food-court.png" alt="Food Court" />
      </swiper-slide>
      <swiper-slide>
        <img src="/images/banners/2.jpg" alt="Food Court" />
      </swiper-slide>
      <swiper-slide>
        <img src="/images/banners/3.jpg" alt="Food Court" />
      </swiper-slide>
    </swiper>

    <button class="nav-btn next-btn" @click="swiperRef?.slidePrev()">
      <i class="fa-solid fa-caret-right"></i>
    </button>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Autoplay, Pagination } from 'swiper/modules'
import 'swiper/css'
import 'swiper/css/pagination'

const SwiperAutoplay = Autoplay
const SwiperPagination = Pagination
const swiperRef = ref(null)

const onSwiper = (swiper) => {
  swiperRef.value = swiper
}
</script>

<style scoped>
.slider-ads-content {
  margin: 12rem auto 0 auto;
  width: 1200px;
  height: 400px;
  border-radius: 50px;
  position: relative;
  padding: 0 60px;
}

.nav-btn {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: var(--primary-orange);
  border: none;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  cursor: pointer;
  z-index: 10;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  font-size: 1.2rem;
  color: var(--white);
  transition: all 0.3s ease;
}

.nav-btn:hover {
  background: var(--gray-light);
  color: var(--primary-color);
}

.prev-btn {
  left: 0;
}

.next-btn {
  right: 0;
}

.slider-ads-content :deep(.swiper) {
  width: 100%;
  height: 100%;
  border-radius: 50px;
  overflow: hidden;
}

.slider-ads-content :deep(.swiper-wrapper) {
  height: 100%;
}

.slider-ads-content :deep(.swiper-slide) {
  width: 100%;
  height: 100%;
  overflow: hidden;
}

.slider-ads-content :deep(.swiper-slide img) {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 50px;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}

.slider-ads-content :deep(.swiper-pagination-bullet) {
  width: 10px;
  height: 10px;
  background: var(--white);
  opacity: 0.5;
}

.slider-ads-content :deep(.swiper-pagination-bullet-active) {
  background: var(--primary-orange);
  opacity: 1;
}
</style>
