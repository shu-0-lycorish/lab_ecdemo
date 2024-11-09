<template>
    <div class="grid grid-cols-12 gap-8 mx-[8%] my-16 pb-[12%]">
        <div class="col-span-12">
            <h1 class="text-4xl">設定</h1>
        </div>

        <div class="col-span-4">
            <NuxtLink to="/setting/profile">
                <div class="flex justify items-center space-x-4 px-6 py-8 bg-white shadow-xl hover:shadow-2xl">
                    <div class="w-12">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                            <path d="M344 144c-3.92 52.87-44 96-88 96s-84.15-43.12-88-96c-4-55 35-96 88-96s92 42 88 96z"
                                fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"
                                stroke-width="24" />
                            <path
                                d="M256 304c-87 0-175.3 48-191.64 138.6C62.39 453.52 68.57 464 80 464h352c11.44 0 17.62-10.48 15.65-21.4C431.3 352 343 304 256 304z"
                                fill="none" stroke="currentColor" stroke-miterlimit="10" stroke-width="24" />
                        </svg>
                    </div>
                    <div class="w-full space-y-2">
                        <h3 class="text-2xl">プロフィール</h3>
                        <div class="flex-1 border-b border-gray-500"></div>
                        <p class="text-xm">ユーザ名やプロフィール画像の変更ができます。</p>
                    </div>
                </div>
            </NuxtLink>
        </div>

        <div class="col-span-4">
            <NuxtLink to="/setting/account">
                <div class="flex justify items-center space-x-4 px-6 py-8 bg-white shadow-xl hover:shadow-2xl">
                    <div class="w-12">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                            <path
                                d="M336 64h32a48 48 0 0148 48v320a48 48 0 01-48 48H144a48 48 0 01-48-48V112a48 48 0 0148-48h32"
                                fill="none" stroke="currentColor" stroke-linejoin="round" stroke-width="24" />
                            <rect x="176" y="32" width="160" height="64" rx="26.13" ry="26.13" fill="none"
                                stroke="currentColor" stroke-linejoin="round" stroke-width="24" />
                        </svg>
                    </div>
                    <div class="w-full space-y-2">
                        <h3 class="text-2xl">アカウント</h3>
                        <div class="flex-1 border-b border-gray-500"></div>
                        <p class="text-xm">支払い方法の設定やアカウントの退会ができます。</p>
                    </div>
                </div>
            </NuxtLink>
        </div>

        <div class="col-span-4">
            <NuxtLink to="/404">
                <div class="flex justify items-center space-x-4 px-6 py-8 bg-white shadow-xl hover:shadow-2xl">
                    <div class="w-12">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                            <path
                                d="M336 64h32a48 48 0 0148 48v320a48 48 0 01-48 48H144a48 48 0 01-48-48V112a48 48 0 0148-48h32"
                                fill="none" stroke="currentColor" stroke-linejoin="round" stroke-width="24" />
                            <rect x="176" y="32" width="160" height="64" rx="26.13" ry="26.13" fill="none"
                                stroke="currentColor" stroke-linejoin="round" stroke-width="24" />
                        </svg>
                    </div>
                    <div class="w-full space-y-2">
                        <h3 class="text-2xl">その他</h3>
                        <div class="flex-1 border-b border-gray-500"></div>
                        <p class="text-xm">その他詳細な設定ができます。</p>
                    </div>
                </div>
            </NuxtLink>
        </div>
    </div>
</template>