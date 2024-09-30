<template>
    <div class="grid grid-cols-12 gap-8 mx-[8%] my-16 pb-[12%]">
        <div class="col-span-12">
            <h1 class="text-4xl">カート</h1>
        </div>

        <div class="grid grid-cols-subgrid gap-8 col-span-12 py-8">
            <div class="col-span-2"></div>
            <div class="col-span-4">商品名</div>
            <div class="col-span-2"></div>
            <div class="col-span-2">数量</div>
            <div class="col-span-2">価格(税込)</div>
            <div class="col-span-12 flex-1 border-b border-gray-500"></div>

            <div v-if="cart.length" class="grid grid-cols-subgrid gap-8 col-span-12">
                <div v-for="singleCart in cart" :key="singleCart.id" class="grid grid-cols-subgrid gap-8 col-span-12 flex items-center">
                    <div class="grid grid-cols-subgrid gap-8 col-span-6 flex items-center">
                        <figure class="col-span-2">
                            <nuxt-img :src="singleCart.image" alt="product-image" format="webp" />
                        </figure>
                        <div class="col-span-4 text-lg font-bold">{{ singleCart.name }}</div>
                    </div>
                    <div class="col-span-2">
                        <NuxtLink :to="singleCart._path">
                            <div class="btn btn-ghost">詳細</div>
                        </NuxtLink>
                    </div>
                    <div class="col-span-2">1</div>
                    <div class="col-span-2">¥ {{ singleCart.price }}</div>
                </div>
            </div>

            <div v-else class="col-span-12 py-4">
                <p class="text-center">カート内に商品はありません。</p>
            </div>

            <div class="col-span-12 flex-1 border-b border-gray-500"></div>
        </div>
    </div>
</template>

<script setup>
import { useState } from '#app'
const cart = useState('cart')
console.log(cart.value)
</script>