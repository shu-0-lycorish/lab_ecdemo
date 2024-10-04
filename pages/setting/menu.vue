<template>
    <div class="grid grid-cols-12 gap-8 mx-[8%] my-16 pb-[12%]">
        <div class="col-span-12">
            <h1 class="text-4xl">設定</h1>
        </div>
        <div class="col-span-4">
            <NuxtLink to="/setting/profile">
                <div class="card bg-base-100 shadow-xl">
                    <figure>
                        <img src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp" alt="Shoes" />
                    </figure>
                    <div class="card-body">
                        <h2 class="card-title">プロフィール</h2>
                        <p>ユーザ名やプロフィール画像の変更ができます。</p>
                    </div>
                </div>
            </NuxtLink>
        </div>
        <button class="col-span-4">
            <a>
                <NuxtLink to="/setting/account">
                    <div class="card bg-base-100 shadow-xl">
                        <figure>
                            <img src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp"
                                alt="Shoes" />
                        </figure>
                        <div class="card-body">
                            <h2 class="card-title">アカウント</h2>
                            <p>支払い方法の設定やアカウントの退会ができます。</p>
                        </div>
                    </div>
                </NuxtLink>
            </a>
        </button>
        <div class="card bg-base-100 col-span-4 shadow-xl">
            <figure>
                <img src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp" alt="Shoes" />
            </figure>
            <div class="card-body">
                <h2 class="card-title">その他設定</h2>
                <p>その他詳細な設定ができます。</p>
            </div>
        </div>
    </div>
</template>