<template>
    <footer>
        <div class="footer bg-base-200 text-base-content px-[8%] py-20 space-x-12">
            <aside class="space-y-4 w-[56vw]">
                <h1 class="text-4xl">ThesisMart</h1>
                <p class="text-lg">Demo EC Site for Thesis</p>
            </aside>
            <nav class="text-xl">
                <a class="link link-hover"><NuxtLink to="/top">TOP</NuxtLink></a>
                <a class="link link-hover"><NuxtLink to="/news">NEWS</NuxtLink></a>
                <a class="link link-hover"><NuxtLink to="/magazine">MAGAZINE</NuxtLink></a>
            </nav>
            <nav class="text-xl">
                <a class="link link-hover"><NuxtLink to="/contact">CONTACT</NuxtLink></a>
                <a class="link link-hover">COMPANY</a>
                <a class="link link-hover">PRIVASY POLISY</a>
            </nav>
        </div>
    </footer>

    <footer class="footer bg-base-200 text-base-content border-base-300 border-t px-[8%] py-10">
        <aside class="grid-flow-col items-center">
            <div>
                <p>©ThesisMart created by Shuhei Kawano</p>
            </div>
        </aside>
    </footer>
</template>