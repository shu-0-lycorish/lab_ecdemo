<template>
    <div class="grid grid-cols-12 relative mx-[8%]">
        <div class="col-span-12">
            <div class="card bg-base-100 shadow-xl">
                <nuxt-img src="/images/0101.jpg" alt="product-image" format="webp" />
            </div>
        </div>
        <div class="absolute bottom-6 left-6 w-4/12">
            <div class="flex flex-col space-y-4 px-6 py-4 bg-white">
                <div>
                    <h2 class="text-4xl text-black">Product Title</h2>
                    <p class="text-black">商品説明の概要が入ります．商品説明の概要が入ります．</p>
                </div>
                <h4 class="text-2xl text-black">¥3,500 (税込)</h4>
            </div>
        </div>
    </div>
</template>