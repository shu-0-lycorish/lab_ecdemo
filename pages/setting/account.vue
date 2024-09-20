<template>
    <div class="grid grid-cols-12 gap-8 mx-[8%] my-16 pb-[12%]">
        <div class="col-span-12">
            <h1 class="text-4xl">アカウント</h1>
        </div>
        <div class="col-span-3 card bg-base-100 shadow-xl">
            <figure>
                <img src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp" alt="Shoes" />
            </figure>
            <div class="card-body">
                <h2 class="card-title">お届け先住所</h2>
            </div>
        </div>
        <div class="col-span-3 card bg-base-100 shadow-xl">
            <figure>
                <img src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp" alt="Shoes" />
            </figure>
            <div class="card-body">
                <h2 class="card-title">お支払い情報</h2>
            </div>
        </div>
        
        <button class="col-span-3">
            <a>
                <NuxtLink to="/setting/deleteAccount">
                    <div class="card bg-base-100 shadow-xl">
                        <figure>
                            <img src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp"
                                alt="Shoes" />
                        </figure>
                        <div class="card-body">
                            <h2 class="card-title">退会</h2>
                        </div>
                    </div>
                </NuxtLink>
            </a>
        </button>
    </div>
</template>