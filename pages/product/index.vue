<template>
    <div>
        <h1 class="text-black text-3xl font-bold">Category</h1>
        <div v-for="singleData in data" :key="singleData.id">
            <div>
                <nuxt-img :src="singleData.image" alt="product-image" format="webp" />
            </div>
            <div>
                <h3>{{ singleData.name }}</h3>
                <p>{{ singleData.price }}</p>
            </div>
        </div>
    </div>
</template>

<script setup>
const { data } = await useAsyncData("productQuery3", () =>
    queryContent("/product").where({categoryId: 2}).sort({productId: -1}).find()
)
</script>
