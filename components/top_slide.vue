<template>
    <div class="grid grid-cols-12 relative mx-[8%]">
        <div class="col-span-12">
            <NuxtLink to="/product/0303">
                <div class="card bg-base-100 shadow-xl">
                    <nuxt-img src="/images/0303.jpg" alt="product-image" format="webp" />
                </div>
                <div class="absolute bottom-6 left-6 w-4/12">
                    <div class="flex flex-col space-y-4 px-6 py-4 bg-white">
                        <div>
                            <h2 class="text-4xl text-black font-light">ProductName0303</h2>
                            <p class="text-black">これは要約文です．これは要約文です．これは要約文です．</p>
                        </div>
                        <h4 class="text-2xl text-black">¥10,000 (税込)</h4>
                    </div>
                </div>
            </NuxtLink>
        </div>
    </div>
</template>