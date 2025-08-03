<template>
    <section class="bg-white py-16 px-4">
        <div class="max-w-7xl mx-auto">
            <h2 class="text-3xl font-bold text-center mb-10">
                iPhone 16 Series
            </h2>

            <div
                class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-6"
            >
                <div
                    v-for="product in products"
                    :key="product.name"
                    class="rounded-2xl p-4 shadow-md hover:shadow-xl transition"
                >
                    <div class="relative mb-3">
                        <img
                            :src="product.image"
                            :alt="product.name"
                            class="w-full h-auto"
                        />
                        <span
                            class="absolute top-2 left-2 bg-gray-100 text-xs text-gray-700 px-2 py-1 rounded"
                        >
                            Trả chậm 0%
                        </span>
                    </div>

                    <h3 class="font-semibold text-sm text-gray-800 mb-1">
                        {{ product.name }}
                    </h3>
                    <p class="text-xs text-gray-500 mb-1">
                        {{ product.display }}
                    </p>
                    <p class="text-xs text-gray-500 mb-2">
                        Kích thước: {{ product.size }}"
                    </p>

                    <!-- Dung lượng -->
                    <div class="flex flex-wrap gap-2 text-sm mb-2">
                        <span
                            v-for="capacity in product.capacities"
                            :key="capacity"
                            class="border border-gray-300 rounded px-2 py-0.5 text-xs"
                        >
                            {{ capacity }}
                        </span>
                    </div>

                    <!-- Giá -->
                    <p class="text-red-600 font-bold text-lg mb-1">
                        {{ product.price }}₫
                    </p>
                    <p class="text-xs line-through text-gray-400 mb-1">
                        {{ product.oldPrice }}₫
                    </p>
                    <p class="text-sm text-green-700 mb-2">
                        Quà {{ product.gift }}
                    </p>

                    <!-- Thông số -->
                    <ul class="text-xs text-gray-700 leading-5 mb-2">
                        <li>Chip: {{ product.chip }}</li>
                        <li>RAM: {{ product.ram }}</li>
                        <li>Dung lượng: {{ product.storage }}</li>
                        <li>Camera sau: {{ product.rearCam }}</li>
                        <li>Camera trước: {{ product.frontCam }}</li>
                        <li>Pin: {{ product.battery }}</li>
                    </ul>

                    <!-- Đánh giá -->
                    <div
                        class="flex items-center justify-between text-xs text-gray-500 mt-2"
                    >
                        <span
                            >⭐ {{ product.rating }} · Đã bán
                            {{ product.sold }}</span
                        >
                        <NuxtLink to="#" class="text-blue-500 hover:underline"
                            >+ So sánh</NuxtLink
                        >
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="bg-white py-16 px-4">
        <div class="max-w-7xl mx-auto">
            <h2 class="text-3xl font-bold text-center mb-10">
                iPhone 15 Series
            </h2>

            <div
                class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-6"
            >
                <div
                    v-for="product in products"
                    :key="product.name"
                    class="rounded-2xl p-4 shadow-md hover:shadow-xl transition"
                >
                    <div class="relative mb-3">
                        <img
                            :src="product.image"
                            :alt="product.name"
                            class="w-full h-auto"
                        />
                        <span
                            class="absolute top-2 left-2 bg-gray-100 text-xs text-gray-700 px-2 py-1 rounded"
                        >
                            Trả chậm 0%
                        </span>
                    </div>

                    <h3 class="font-semibold text-sm text-gray-800 mb-1">
                        {{ product.name }}
                    </h3>
                    <p class="text-xs text-gray-500 mb-1">
                        {{ product.display }}
                    </p>
                    <p class="text-xs text-gray-500 mb-2">
                        Kích thước: {{ product.size }}"
                    </p>

                    <!-- Dung lượng -->
                    <div class="flex flex-wrap gap-2 text-sm mb-2">
                        <span
                            v-for="capacity in product.capacities"
                            :key="capacity"
                            class="border border-gray-300 rounded px-2 py-0.5 text-xs"
                        >
                            {{ capacity }}
                        </span>
                    </div>

                    <!-- Giá -->
                    <p class="text-red-600 font-bold text-lg mb-1">
                        {{ product.price }}₫
                    </p>
                    <p class="text-xs line-through text-gray-400 mb-1">
                        {{ product.oldPrice }}₫
                    </p>
                    <p class="text-sm text-green-700 mb-2">
                        Quà {{ product.gift }}
                    </p>

                    <!-- Thông số -->
                    <ul class="text-xs text-gray-700 leading-5 mb-2">
                        <li>Chip: {{ product.chip }}</li>
                        <li>RAM: {{ product.ram }}</li>
                        <li>Dung lượng: {{ product.storage }}</li>
                        <li>Camera sau: {{ product.rearCam }}</li>
                        <li>Camera trước: {{ product.frontCam }}</li>
                        <li>Pin: {{ product.battery }}</li>
                    </ul>

                    <!-- Đánh giá -->
                    <div
                        class="flex items-center justify-between text-xs text-gray-500 mt-2"
                    >
                        <span
                            >⭐ {{ product.rating }} · Đã bán
                            {{ product.sold }}</span
                        >
                        <NuxtLink to="#" class="text-blue-500 hover:underline"
                            >+ So sánh</NuxtLink
                        >
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
const products = [
    {
        name: "iPhone 16 Pro Max 256GB",
        display: "Super Retina XDR",
        size: "6.9",
        image: "images/ip_16pm.png",
        capacities: ["256GB", "512GB", "1TB"],
        price: "30.090.000",
        oldPrice: "34.290.000",
        gift: "500.000",
        chip: "Apple A18 Pro 6 nhân",
        ram: "8 GB",
        storage: "256 GB",
        rearCam: "48 MP & Phụ 48 MP, 12 MP",
        frontCam: "12 MP",
        battery: "33 giờ, Sạc 20 W",
        rating: "4.9",
        sold: "230,3k",
    },
    {
        name: "iPhone 16 Pro 128GB",
        display: "Super Retina XDR",
        size: "6.3",
        image: "images/ip_16plus.png",
        capacities: ["128GB", "256GB", "512GB", "1TB"],
        price: "25.090.000",
        oldPrice: "28.300.000",
        gift: "500.000",
        chip: "Apple A18 Pro 6 nhân",
        ram: "8 GB",
        storage: "128 GB",
        rearCam: "48 MP & Phụ 48 MP, 12 MP",
        frontCam: "12 MP",
        battery: "27 giờ, Sạc 20 W",
        rating: "4.9",
        sold: "25,6k",
    },
    {
        name: "iPhone 16 Plus 128GB",
        display: "Super Retina XDR",
        size: "6.7",
        image: "images/ip_15pm.png",
        capacities: ["128GB", "256GB", "512GB"],
        price: "22.190.000",
        oldPrice: "25.490.000",
        gift: "500.000",
        chip: "Apple A18 6 nhân",
        ram: "8 GB",
        storage: "128 GB",
        rearCam: "48 MP & Phụ 12 MP",
        frontCam: "12 MP",
        battery: "27 giờ, Sạc 20 W",
        rating: "4.9",
        sold: "17,1k",
    },
    {
        name: "iPhone 16 128GB",
        display: "Super Retina XDR",
        size: "6.1",
        image: "images/ip_15.png",
        capacities: ["128GB", "256GB"],
        price: "19.090.000",
        oldPrice: "22.490.000",
        gift: "500.000",
        chip: "Apple A18 6 nhân",
        ram: "8 GB",
        storage: "128 GB",
        rearCam: "48 MP & Phụ 12 MP",
        frontCam: "12 MP",
        battery: "22 giờ, Sạc 20 W",
        rating: "4.9",
        sold: "13,6k",
    },
    {
        name: "iPhone 16e 128GB",
        display: "Super Retina XDR",
        size: "6.1",
        image: "images/ip_16pm.png",
        capacities: ["128GB", "256GB", "512GB"],
        price: "16.290.000",
        oldPrice: "16.690.000",
        gift: "500.000",
        chip: "Apple A18 6 nhân",
        ram: "8 GB",
        storage: "128 GB",
        rearCam: "48 MP",
        frontCam: "12 MP",
        battery: "26 giờ, Sạc 20 W",
        rating: "4.9",
        sold: "3,9k",
    },
];
</script>
