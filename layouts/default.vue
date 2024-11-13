<template>
    <div class="flex flex-col min-h-screen">
        <div v-if="route.path !== '/'">
            <Header />
        </div>
        <main class="flex-grow"><slot/></main>
        <div v-if="route.path !== '/'">
            <Footer />
        </div>
    </div>
</template>

<script setup>
const route = useRoute()
</script>