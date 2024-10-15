<template>
    <div class="grid grid-cols-12 gap-8 mx-[8%] my-16 pb-[12%]">
        <div class="col-span-12">
            <h1 class="text-4xl">マガジン</h1>
        </div>

        <div class="grid grid-cols-subgrid gap-8 col-span-12 py-8 flex items-center">
            <div class="col-span-12 flex-1 border-b border-gray-500"></div>
            <div class="col-span-3">
                <nuxt-img src="/images/0302.jpg" alt="magazine-image" format="webp" />
            </div>
            <div class="col-start-5 col-span-2">
                <h4 class="text-xl">2024.10.11</h4>
            </div>
            <div class="col-span-6">
                <h4 class="text-xl">今週のおすすめ商品</h4>
            </div>

            <div class="col-span-12 flex-1 border-b border-gray-500"></div>

            <div class="col-span-3">
                <nuxt-img src="/images/0202.jpg" alt="magazine-image" format="webp" />
            </div>
            <div class="col-start-5 col-span-2">
                <h4 class="text-xl">2024.10.04</h4>
            </div>
            <div class="col-span-6">
                <h4 class="text-xl">今週のおすすめ商品</h4>
            </div>

            <div class="col-span-12 flex-1 border-b border-gray-500"></div>
        </div>
    </div>
</template>