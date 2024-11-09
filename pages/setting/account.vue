<template>
    <div class="grid grid-cols-12 gap-8 mx-[8%] my-16 pb-[12%]">
        <div class="col-span-12">
            <h1 class="text-4xl">アカウント</h1>
        </div>

        <div class="col-span-4">
            <NuxtLink to="/404">
                <div class="flex justify items-center space-x-4 px-6 py-8 bg-white shadow-xl hover:shadow-2xl">
                    <div class="w-12">
                        <svg xmlns="http://www.w3.org/2000/svg" class="ionicon" viewBox="0 0 512 512">
                            <path
                                d="M80 212v236a16 16 0 0016 16h96V328a24 24 0 0124-24h80a24 24 0 0124 24v136h96a16 16 0 0016-16V212"
                                fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"
                                stroke-width="32" />
                            <path d="M480 256L266.89 52c-5-5.28-16.69-5.34-21.78 0L32 256M400 179V64h-48v69" fill="none"
                                stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"
                                stroke-width="32" />
                        </svg>
                    </div>
                    <div class="w-full space-y-2">
                        <h3 class="text-2xl">お届け先住所</h3>
                        <div class="flex-1 border-b border-gray-500"></div>
                        <p class="text-xm">商品のお届け先の設定や変更ができます。</p>
                    </div>
                </div>
            </NuxtLink>
        </div>

        <div class="col-span-4">
            <NuxtLink to="/404">
                <div class="flex justify items-center space-x-4 px-6 py-8 bg-white shadow-xl hover:shadow-2xl">
                    <div class="w-12">
                        <svg xmlns="http://www.w3.org/2000/svg" class="ionicon" viewBox="0 0 512 512">
                            <rect x="48" y="96" width="416" height="320" rx="56" ry="56" fill="none"
                                stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"
                                stroke-width="32" />
                            <path fill="none" stroke="currentColor" stroke-linejoin="round" stroke-width="60"
                                d="M48 192h416M128 300h48v20h-48z" />
                        </svg>
                    </div>
                    <div class="w-full space-y-2">
                        <h3 class="text-2xl">お支払い情報</h3>
                        <div class="flex-1 border-b border-gray-500"></div>
                        <p class="text-xm">お支払い情報の設定や変更ができます。</p>
                    </div>
                </div>
            </NuxtLink>
        </div>

        <div class="col-span-4">
            <div v-if="siteType !== 'B'">
                <NuxtLink to="/setting/deleteAccount">
                    <div class="flex justify items-center space-x-4 px-6 py-8 bg-white shadow-xl hover:shadow-2xl">
                        <div class="w-12">
                            <svg xmlns="http://www.w3.org/2000/svg" class="ionicon" viewBox="0 0 512 512">
                                <path d="M376 144c-3.92 52.87-44 96-88 96s-84.15-43.12-88-96c-4-55 35-96 88-96s92 42 88 96z"
                                    fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"
                                    stroke-width="32" />
                                <path
                                    d="M288 304c-87 0-175.3 48-191.64 138.6-2 10.92 4.21 21.4 15.65 21.4H464c11.44 0 17.62-10.48 15.65-21.4C463.3 352 375 304 288 304z"
                                    fill="none" stroke="currentColor" stroke-miterlimit="10" stroke-width="32" />
                                <path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"
                                    stroke-width="32" d="M144 232H32" />
                            </svg>
                        </div>
                        <div class="w-full space-y-2">
                            <h3 class="text-2xl">退会</h3>
                            <div class="flex-1 border-b border-gray-500"></div>
                            <p class="text-xm">サービスからの退会、アカウントの削除ができます。</p>
                        </div>
                    </div>
                </NuxtLink>
            </div>
            <div v-if="siteType === 'B'">
                <NuxtLink to="/setting/d_deleteAccount_1">
                    <div class="flex justify items-center space-x-4 px-6 py-8 bg-white shadow-xl hover:shadow-2xl">
                        <div class="w-12">
                            <svg xmlns="http://www.w3.org/2000/svg" class="ionicon" viewBox="0 0 512 512">
                                <path d="M376 144c-3.92 52.87-44 96-88 96s-84.15-43.12-88-96c-4-55 35-96 88-96s92 42 88 96z"
                                    fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"
                                    stroke-width="32" />
                                <path
                                    d="M288 304c-87 0-175.3 48-191.64 138.6-2 10.92 4.21 21.4 15.65 21.4H464c11.44 0 17.62-10.48 15.65-21.4C463.3 352 375 304 288 304z"
                                    fill="none" stroke="currentColor" stroke-miterlimit="10" stroke-width="32" />
                                <path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"
                                    stroke-width="32" d="M144 232H32" />
                            </svg>
                        </div>
                        <div class="w-full space-y-2">
                            <h3 class="text-2xl">退会</h3>
                            <div class="flex-1 border-b border-gray-500"></div>
                            <p class="text-xm">サービスからの退会、アカウントの削除ができます。</p>
                        </div>
                    </div>
                </NuxtLink>
            </div>
        </div>
    </div>
</template>

<script setup>
import { useState } from '#app'
const siteType = useState('siteType')
</script>