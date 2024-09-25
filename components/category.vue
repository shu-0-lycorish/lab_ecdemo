<template>
    <div class="grid grid-cols-12 gap-8 my-16 relative mx-[8%]">
        <div class="col-span-12 flex space-x-3">
            <h1 class="text-black text-4xl font-bold">Category</h1>
            <p class="self-center text-xm font-bold">カテゴリー</p>
        </div>
        <div class="grid grid-cols-subgrid col-span-12">
            <div v-for="singleData in data" :key="singleData.id" class="col-span-4 space-y-4">
                <NuxtLink :to="'/product/' + [singleData.categoryId]">
                <div>
                    <nuxt-img :src="singleData.image" alt="product-image" format="webp" />
                </div>
                <div class="text-3xl">
                    <h2 v-if="singleData.categoryId === 1">Light</h2>
                    <h2 v-if="singleData.categoryId === 2">Clock</h2>
                    <h2 v-if="singleData.categoryId === 3">Sofa</h2>
                </div>
                </NuxtLink>
            </div>
        </div>
    </div>
</template>

<script setup>
const { data } = await useAsyncData("productQuery", () =>
    queryContent("/product").where({ productId: 1 }).find()
)
</script>