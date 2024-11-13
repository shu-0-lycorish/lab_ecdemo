<template>
    <div class="grid grid-cols-12 gap-8 mx-[8%] my-32 grid place-items-center text-center">
        <div class="col-start-6 col-span-2 w-full">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                <path d="M448 256c0-106-86-192-192-192S64 150 64 256s86 192 192 192 192-86 192-192z" fill="none"
                    stroke="currentColor" stroke-miterlimit="10" stroke-width="32" />
                <path d="M250.26 166.05L256 288l5.73-121.95a5.74 5.74 0 00-5.79-6h0a5.74 5.74 0 00-5.68 6z" fill="none"
                    stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="32" />
                <path d="M256 367.91a20 20 0 1120-20 20 20 0 01-20 20z" />
            </svg>
        </div>
        <div class="col-span-12">
            <h1 class="text-4xl">Error 404</h1>
        </div>
        <div class="col-span-12 space-y-2">
            <h4 class="text-xl">このページは実験タスク対象外のため存在しません。</h4>
            <h4 class="text-xl">前のページに戻る、または下記のボタンからトップページに戻り、実験タスクを続けてください。</h4>
        </div>
        <div class="col-start-6 col-span-2 py-8">
            <NuxtLink to="/top">
                <button class="btn btn-active text-lg w-full">トップページに戻る</button>
            </NuxtLink>
        </div>
    </div>
</template>