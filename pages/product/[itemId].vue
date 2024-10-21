<template>
    <div :key="renderKey" class="grid grid-cols-12 gap-8 my-16 relative mx-[8%] min-h-[52vh] place-content-start">
        <div class="col-span-7">
            <nuxt-img :src="data.image" alt="blog-image" format="webp" />
        </div>
        <div class="col-span-5 content-center space-y-8">
            <div class="space-y-2">
                <h2 class="text-3xl text-black">{{ data.name }}</h2>
                <p class="text-lg text black">{{ data.summary }}</p>
            </div>

            <h4 class="text-xl text-black">¥ {{ data.price }} (税込)</h4>

            <div v-if="siteType !== 'A' && siteType === 'B'">
                <p class="text-xm font-bold text-red-500">{{ data.darkData }}</p>
            </div>


            <div>
                <div v-if="cartButton">
                    <button class="btn btn-error text-lg">カートに追加しました</button>
                </div>
                <div v-else>
                    <button v-on:click="addCart" class="btn btn-primary text-lg">カートに追加する</button>
                </div>
            </div>

        </div>
        <div class="col-span-12 my-16 space-y-8">
            <h2 class="text-3xl">商品説明</h2>
            <div>
                <ContentDoc />
            </div>
        </div>

    </div>
</template>

<script setup>
import { ref } from 'vue'
import { useState } from '#app'

const cart = useState('cart')
// const [cart, setCart] = useState([])

const { data } = await useAsyncData(useRoute().path, () =>
    queryContent(useRoute().path).findOne()
)

console.log(useRoute().path)
// await console.log(data.value.itemId)

let cartButton = false

const renderKey = ref(0)

const addCart = () => {
    cart.value.push(data.value)
    cartButton = true
    renderKey.value = renderKey.value + 1

    console.log(cart.value[0].itemId)
}

const siteType = useState('siteType')
</script>