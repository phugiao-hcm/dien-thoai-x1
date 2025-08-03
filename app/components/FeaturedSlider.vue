<template>
  <section class="py-12 px-4 bg-black text-white">
    <h2 class="text-3xl md:text-4xl font-semibold text-center mb-8">
      Get to know iPhone
    </h2>

    <Swiper
      :slides-per-view="1.3"
      :space-between="16"
      :breakpoints="{
        640: { slidesPerView: 1.3 },
        768: { slidesPerView: 2.3 },
        1024: { slidesPerView: 3.3 },
        1280: { slidesPerView: 4.5 },
      }"
      grab-cursor
    >
      <SwiperSlide
        v-for="(item, index) in iphoneCards"
        :key="index"
        class="rounded-xl overflow-hidden bg-white text-black"
      >
        <img
          :src="item.image"
          :alt="item.title"
          class="w-full h-60 object-cover"
        />
        <div class="p-4">
          <h3 class="text-xl font-semibold mb-1">{{ item.title }}</h3>
          <p class="text-sm">{{ item.description }}</p>
        </div>
      </SwiperSlide>
    </Swiper>
  </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";

const iphoneCards = [
  {
    title: "iPhone 15 Pro",
    description: "Titanium. So strong. So light. So Pro.",
    image: "images/1.png",
  },
  {
    title: "Dynamic Island",
    description: "Stay in the know. On the go.",
    image: "images/2.png",
  },
  {
    title: "Camera Power",
    description: "Capture incredible detail with the 48MP main camera.",
    image: "images/3.png",
  },
  {
    title: "A17 Pro chip",
    description: "The biggest leap in iPhone graphics performance.",
    image: "images/4.png",
  },
  {
    title: "USB‑C",
    description: "The universal connector.",
    image: "images/5.png",
  },
];
</script>

<style scoped>
/* Optional: smooth scroll effect */
.swiper {
  padding-bottom: 20px;
}
</style>
