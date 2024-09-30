<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>

<script setup>
import { useState } from '#app'

const cart = useState('cart', () => ([]))


</script>