<template>
    <div class="grid grid-cols-12 gap-8 mx-[8%] my-16 pb-[12%]">
        <div class="col-span-12">
            <h1 class="text-4xl">カート</h1>
        </div>

        <div class="grid grid-cols-subgrid gap-8 col-span-12">
            <div class="col-span-2"></div>
            <div class="col-span-4">商品名</div>
            <div class="col-span-2"></div>
            <div class="col-span-2">数量</div>
            <div class="col-span-2">価格(税込)</div>
            <div class="col-span-12 flex-1 border-b border-gray-500"></div>

            <div v-if="cart.length" class="grid grid-cols-subgrid gap-8 col-span-12">
                <div v-for="singleCart in cart" :key="singleCart.id"
                    class="grid grid-cols-subgrid gap-8 col-span-12 flex items-center">
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

            <div v-if="cart.length && siteType === 'A'" class="grid grid-cols-subgrid gap-8 col-span-12 flex items-center">
                <div class="col-start-9 col-span-2">
                    <p class="font-bold">合計金額(税込)</p>
                </div>
                <div class="col-start-11 col-span-2">
                    <h3 class="text-2xl font-bold">¥ {{ totalPrice }}</h3>
                </div>
            </div>

            <div v-if="cart.length && siteType === 'B'" class="grid grid-cols-subgrid gap-8 col-span-12 flex items-center">
                <div class="col-start-9 col-span-2">
                    <p class="font-bold line-through">合計金額(税込)</p>
                </div>
                <div class="col-start-11 col-span-2">
                    <h3 class="text-2xl font-bold line-through">¥ {{ totalPrice }}</h3>
                </div>
            </div>

            <div v-if="cart.length && siteType === 'B'" class="grid grid-cols-subgrid gap-8 col-span-12 flex items-center">
                <div class="col-start-9 col-span-2">
                    <p class="font-bold text-red-500">セール適用後合計(税込)</p>
                </div>
                <div class="col-start-11 col-span-2">
                    <h3 class="text-2xl font-bold text-red-500">¥ {{ totalPrice * 0.9}}</h3>
                </div>
            </div>


        </div>

        <div class="col-end-12 col-span-3">
            <div v-if="cart.length && siteType === 'A' && siteType !== 'B'" class="form-control">
                <label class="label cursor-pointer">
                    <span class="text-xm">メールマガジンを購読する</span>
                    <input type="checkbox" class="checkbox" />
                </label>
            </div>
            <div v-if="cart.length && siteType !== 'A' && siteType === 'B'" class="form-control">
                <label class="label cursor-pointer">
                    <span class="text-xm">メールマガジンを購読しない</span>
                    <input type="checkbox" class="checkbox" />
                </label>
                <p class="text-xs">
                購入手続きを完了すると<NuxtLink to="/terms" class="underline hover:text-blue-500">利用規約</NuxtLink>に同意されたものとみなします。
            </p>
            </div>
        </div>

        <div v-if="cart.length" class="col-end-12 col-span-3">
            <NuxtLink to="compBuying">
                <button @click="buyCart" class="btn btn-primary text-lg w-full">購入する</button>
            </NuxtLink>
        </div>
    </div>
</template>

<script setup>
import { useState } from '#app'
const cart = useState('cart')
const siteType = useState('siteType')

let totalPrice = 0

/*
for (var i=0; i<cart.value.length; i++){
    totalPrice += cart.value[i].price
}
*/

for (let item of cart.value) {
    totalPrice += item.price
}

const buyCart = () => {
    cart.value.length = 0
}
</script>