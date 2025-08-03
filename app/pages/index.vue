<template>
    <div>
        <HeroSection />
        <FeatureSection />
        <ProductSection />
        <ProductGrid />
        <FeaturedSlider />
    </div>
</template>

<script setup>
import HeroSection from "@/components/HeroSection.vue";
import FeaturedSlider from "@/components/FeaturedSlider.vue";
import FeatureSection from "./FeatureSection.vue";
import ProductGrid from "./ProductGrid.vue";
import ProductSection from "./ProductSection.vue";
</script>
