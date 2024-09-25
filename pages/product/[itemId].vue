<template>
    <div>
        <div>
            <nuxt-img :src="data.image" alt="blog-image" format="webp" />
        </div>
        <div>  
            <div>               
                <h1>{{ data.name }}</h1>
                <p>{{ data.price }}</p> 
                <ContentDoc />
            </div> 
        </div>
    </div>
</template>

<script setup>
const { data } = await useAsyncData(useRoute().path, () =>
    queryContent(useRoute().path).findOne()
)

console.log(useRoute().path)
</script>