<template>
    <div class="grid grid-cols-12 gap-8 my-16 relative mx-[8%]">
        <div class="col-span-12 flex space-x-3">
            <h1 class="text-black text-4xl font-bold">Category</h1>
            <p class="self-center text-xm font-bold">カテゴリー</p>
        </div>
        <div class="grid grid-cols-subgrid col-span-12">
            <div class="col-span-4 space-y-4">
                <nuxt-img src="/images/0101.jpg" alt="product-image" format="webp" />
                <h2 class="text-3xl">Light</h2>
            </div>
            <div class="col-span-4 space-y-4">
                <nuxt-img src="/images/0201.jpg" alt="product-image" format="webp" />
                <h2 class="text-3xl">Clock</h2>
            </div>
            <div class="col-span-4 space-y-4">
                <nuxt-img src="/images/0301.jpg" alt="product-image" format="webp" />
                <h2 class="text-3xl">Sofa</h2>
            </div>
        </div>
    </div>
</template>