<template>
    <header>
        <div class="navbar px-6 py-4 bg-base-100">
            <div class="navbar-start">
                <ul class="menu menu-horizontal px-2 w-[24.5rem]">
                    <li>
                        <details>
                            <summary>PRODUCTS</summary>
                            <ul class="bg-base-100 rounded-t-none p-1">
                                <li><a>Light</a></li>
                                <li><a>Clock</a></li>
                                <li><a>Sofa</a></li>
                            </ul>
                        </details>
                    </li>
                    <li><a>NEWS</a></li>
                    <li><a>MAGAZINE</a></li>
                    <li><a>GUIDE</a></li>
                </ul>
            </div>
            <div class="navbar-center">
                <div>
                    <a class="btn btn-ghost text-3xl"><NuxtLink to="/">ThesisMart</NuxtLink></a>
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
                        <li><a class="justify-between">プロフィール</a></li>
                        <li><NuxtLink to="/setting/menu">設定</NuxtLink></li>
                        <li><a>ログアウト</a></li>
                    </ul>
                </div>
                <div>
                    <div tabindex="0" role="button" class="btn btn-ghost btn-circle">
                        <div class="indicator">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24"
                                stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z" />
                            </svg>
                            <span class="badge badge-sm indicator-item">3</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>