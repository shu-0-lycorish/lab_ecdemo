<template>
    <header>
        <div class="navbar px-6 py-4 bg-base-100 z-50">
            <div class="navbar-start">
                <ul class="menu menu-horizontal px-2 w-[26rem]">
                    <li>
                        <details>
                            <summary>PRODUCTS</summary>
                            <ul class="bg-base-100 rounded-t-none w-[9rem] pl-1 z-40">
                                <li><NuxtLink to="/category/1"><a>Light - 照明</a></NuxtLink></li>
                                <li><NuxtLink to="/category/2"><a>Clock - 時計</a></NuxtLink></li>
                                <li><NuxtLink to="/category/3"><a>Sofa - ソファ</a></NuxtLink></li>
                            </ul>
                        </details>
                    </li>
                    <li><NuxtLink to="/news"><a>NEWS</a></NuxtLink></li>
                    <li><NuxtLink to="/magazine"><a>MAGAZINE</a></NuxtLink></li>
                    <li><NuxtLink to="/contact"><a>CONTACT</a></NuxtLink></li>
                </ul>
            </div>
            <div class="navbar-center">
                <div>
                    <NuxtLink to="/top"><a class="btn btn-ghost text-3xl">ThesisMart</a></NuxtLink>
                </div>
            </div>
            <div class="navbar-end space-x-4">
                <div class="dropdown dropdown-end">
                    <div tabindex="0" role="button" class="btn btn-ghost btn-circle avatar">
                        <div class="w-10 rounded-full">
                            <img alt="Tailwind CSS Navbar component"
                                src="https://img.daisyui.com/images/stock/photo-1534528741775-53994a69daeb.webp" />
                        </div>
                    </div>
                    <ul tabindex="0"
                        class="menu menu-sm dropdown-content bg-base-100 rounded-box z-[1] mt-3 w-52 p-2 shadow">
                        <li><NuxtLink to="/setting/profile">プロフィール</NuxtLink></li>
                        <li><NuxtLink to="/setting/menu">設定</NuxtLink></li>
                        <li><NuxtLink to="/"><a>ログアウト</a></NuxtLink></li>
                    </ul>
                </div>
                <div>
                    <NuxtLink to="/cart">
                        <div tabindex="0" role="button" class="btn btn-ghost btn-circle">
                            <div class="indicator">
                                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24"
                                    stroke="currentColor">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                        d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z" />
                                </svg>
                                <span class="badge badge-sm indicator-item">{{ cart.length }}</span>
                            </div>
                        </div>
                    </NuxtLink>
                </div>
            </div>
        </div>
        <div v-if="siteType !== 'A' && siteType === 'B'">
            <DCountdown />
        </div>
    </header>
</template>

<script setup>
import { useState } from '#app'
const cart = useState('cart')
const siteType = useState('siteType')
</script>