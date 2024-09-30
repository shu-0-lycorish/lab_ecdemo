<template>
    <div class="grid grid-cols-12 gap-8 my-16 relative mx-[8%] min-h-[52vh] place-content-start">
        <div class="col-span-7">
            <nuxt-img :src="data.image" alt="blog-image" format="webp" />
        </div>
        <div class="col-span-5 content-center space-y-8">
            <div class="space-y-2">
                <h2 class="text-3xl text-black">{{ data.name }}</h2>
                <p class="text-lg text black">{{ data.summary }}</p>
                <p>{{ data.itemId }}</p>
            </div>
            <h4 class="text-xl text-black">¥ {{ data.price }}  (税込)</h4>
            <div>
                <NuxtLink to="/">
                    <button @click="addCart" class="btn btn-primary text-lg">カートに入れる</button>
                </NuxtLink>
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
import { useState } from '#app'
const cart = useState('cart')
// const [cart, setCart] = useState([])

const { data } = await useAsyncData(useRoute().path, () =>
    queryContent(useRoute().path).findOne()
)

console.log(useRoute().path)
// await console.log(data.value.itemId)

const addCart = () => {
    cart.value.push(data.value)

    console.log(cart.value[0].itemId)
}
</script>