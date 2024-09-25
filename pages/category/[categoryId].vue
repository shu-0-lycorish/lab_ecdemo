<template>
    <div>
        <h1 class="text-black text-3xl font-bold">Category</h1>
        <div v-for="singleData in data" :key="singleData.id">
            <NuxtLink :to="singleData._path">
                <div>
                    <nuxt-img :src="singleData.image" alt="product-image" format="webp" />
                </div>
                <div>
                    <h3>{{ singleData.name }}</h3>
                    <p>{{ singleData.price }}</p>
                </div>
            </NuxtLink>
        </div>
    </div>
</template>

<script setup>
const path = useRoute().path
var category = path.replace('/category/', '')

const { data } = await useAsyncData("productQuery2", () =>
    queryContent("/product").where({categoryId: Number(category)}).find()
)

console.log(category)
</script>