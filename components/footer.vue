<template>
    <footer>
        <div class="footer bg-base-200 text-base-content px-[8%] py-20 space-x-12">
            <aside class="space-y-4 w-[56vw]">
                <h1 class="text-4xl">ThesisMart</h1>
                <p>Demo EC Site for Thesis</p>
            </aside>
            <nav>
                <a class="link link-hover text-xl"><NuxtLink to="/top">TOP</NuxtLink></a>
                <a class="link link-hover text-xl"><NuxtLink to="/news">NEWS</NuxtLink></a>
                <a class="link link-hover text-xl"><NuxtLink to="/magazine">MAGAZINE</NuxtLink></a>
            </nav>
            <nav>
                <a class="link link-hover text-xl"><NuxtLink to="/contact">CONTACT</NuxtLink></a>
                <a class="link link-hover text-xl">COMPANY</a>
                <a class="link link-hover text-xl">PRIVASY POLISY</a>
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