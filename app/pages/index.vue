<template>
  <div>
    <HeroSection />
    <FeatureSection />
    <ProductGrid />
    <FeaturedSlider />
  </div>
</template>

<script setup>
import HeroSection from "@/components/HeroSection.vue";
import FeaturedSlider from "@/components/FeaturedSlider.vue";
import FeatureSection from "./FeatureSection.vue";
import ProductGrid from "./ProductGrid.vue";
</script>
