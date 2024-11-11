<template>
    <div class="grid grid-cols-12 gap-8 my-16 relative mx-[8%]">
        <div class="col-span-12 flex space-x-3">
            <h1 class="text-black text-4xl font-light">Category</h1>
            <p class="self-center text-xm font-bold">カテゴリー</p>
        </div>
        <div class="grid grid-cols-subgrid col-span-12">
            <div v-for="singleData in data" :key="singleData.id" class="col-span-4 space-y-4">
                <NuxtLink :to="'/category/' + [singleData.categoryId]">
                    <div class="shadow-xl hover:shadow-2xl">
                        <nuxt-img :src="singleData.image" alt="product-image" format="webp" />
                    </div>
                    <div class="px-4 py-2">
                        <div v-if="singleData.categoryId === 1" class="flex space-x-3">
                            <h2 class="text-3xl font-light">Light</h2>
                            <p class="self-center text-xm font-light">- 照明</p>
                        </div>
                        <div v-if="singleData.categoryId === 2" class="flex space-x-3">
                            <h2 class="text-3xl font-light">Clock</h2>
                            <p class="self-center text-xm font-light">- 時計</p>
                        </div>
                        <div v-if="singleData.categoryId === 3" class="flex space-x-3">
                            <h2 class="text-3xl font-light">Sofa</h2>
                            <p class="self-center text-xm font-light">- ソファ</p>
                        </div>
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