<template>
    <div class="grid grid-cols-12 gap-8 my-16 relative mx-[8%] min-h-[52vh] place-content-start">
        <div class="col-span-12">
            <div class="text-black text-3xl font-bold">
                <h2 v-if="category === 1">Light</h2>
                <h2 v-if="category === 2">Clock</h2>
                <h2 v-if="category === 3">Sofa</h2>
            </div>
        </div>
        <div class="grid grid-cols-subgrid col-span-12">
            <div v-for="singleData in data" :key="singleData.id" class="col-span-4 space-y-4">
                <NuxtLink :to="singleData._path">
                    <div class="card bg-base-100 shadow-xl">
                        <figure>
                            <nuxt-img :src="singleData.image" alt="product-image" format="webp" />
                        </figure>
                        <div class="card-body">
                            <h3 class="text-2xl text-black">{{ singleData.name }}</h3>
                            <div>
                                <div v-if="siteType !== 'A' && siteType === 'B'">
                                    <p class="text-xm font-bold text-red-500">{{ singleData.darkData }}</p>
                                </div>
                                <p class="text-lg text-black">¥ {{ singleData.price }}  (税込)</p>
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

const { data } = await useAsyncData("productQuery2", () =>
    queryContent("/product").where({ categoryId: category }).find()
)

console.log(category)

const siteType = useState('siteType')
</script>