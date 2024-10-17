<template>
    <span class="countdown font-mono text-6xl">
        <span :style="'--value:' + minutes + ';'"></span>
        :
        <span :style="'--value:' + seconds + ';'"></span>
    </span>
</template>
<script setup>
const totalTime = 600
const counter = ref(totalTime)
const minutes = ref(computed(() => Math.floor(counter.value / 60)))
const seconds = ref(computed(() => counter.value % 60))

onMounted(() => {
    setInterval(() => {
        if(counter.value > 0) {
            counter.value = counter.value - 1
        }
        else {
            counter.value += 600
        }
    }, 1000);
})
</script>