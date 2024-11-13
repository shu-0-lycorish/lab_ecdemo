<template>
    <div class="w-full mb-8 py-2 bg-amber-100">
        <div class="grid justify-items-center">
            <p class="font-bold">下記時間内の購入で合計金額から10％OFF！</p>
            <div class="flex items-center">
                <p>残り　</p>
                <span class="countdown font-mono text-4xl text-red-500">
                    <span :style="'--value:' + minutes + ';'"></span>
                    :
                    <span :style="'--value:' + seconds + ';'"></span>
                </span>
            </div>
        </div>
    </div>
</template>
<script setup>
const totalTime = 600
const counter = ref(totalTime)
const minutes = ref(computed(() => Math.floor(counter.value / 60)))
const seconds = ref(computed(() => counter.value % 60))

onMounted(() => {
    setInterval(() => {
        if (counter.value > 0) {
            counter.value = counter.value - 1
        }
        else {
            counter.value += 600
        }
    }, 1000);
})
</script>