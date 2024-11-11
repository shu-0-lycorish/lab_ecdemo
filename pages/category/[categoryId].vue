<template>
    <div class="grid grid-cols-12 gap-8 my-12 relative mx-[8%]">
        <div class="col-span-12">
            <div v-if="category === 1" class="flex space-x-3">
                <h2 class="text-3xl font-light">Light</h2>
                <p class="self-center text-xm font-light">- 照明</p>
            </div>
            <div v-if="category === 2" class="flex space-x-3">
                <h2 class="text-3xl font-light">Clock</h2>
                <p class="self-center text-xm font-light">- 時計</p>
            </div>
            <div v-if="category === 3" class="flex space-x-3">
                <h2 class="text-3xl font-light">Sofa</h2>
                <p class="self-center text-xm font-light">- ソファ</p>
            </div>
        </div>
        <div class="grid grid-cols-subgrid col-span-12">
            <div v-for="singleData in data" :key="singleData.id" class="col-span-4 space-y-4">
                <NuxtLink :to="singleData._path">
                    <div class="shadow-xl">
                        <nuxt-img :src="singleData.image" alt="product-image" format="webp" />
                        <div class="px-5 py-4">
                            <h3 class="text-2xl text-black font-light">{{ singleData.name }}</h3>
                            <div>
                                <div v-if="siteType !== 'A' && siteType === 'B' && category === 1">
                                    <p class="text-xm font-bold text-red-500">{{ singleData.darkData }}</p>
                                </div>
                                <p class="text-lg text-black">¥ {{ singleData.price }} (税込)</p>
                            </div>
                        </div>
                    </div>
                </NuxtLink>
            </div>
        </div>
    </div>
</template>

<script setup>
import { useState } from '#app'

const path = useRoute().path
var category = Number(path.replace('/category/', ''))
const siteType = useState('siteType')

const { data } = await useAsyncData("productQuery2", () =>
    queryContent("/product").where({ categoryId: category }).find()
)
</script>