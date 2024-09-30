<template>
    <div class="grid grid-cols-12 gap-8 my-16 pb-[6%] relative mx-[8%]">
        <div class="col-span-12">
            <h1 class="text-4xl">カート</h1>
        </div>
        <div class="col-span-12 py-14">
            <div class="flex flex-col space-y-4">
                <p class="text-lg">
                    購入が完了しました。ご利用いただき誠にありがとうございます．
                </p>
            </div>
        </div>
        <div class="col-start-6 col-span-2">
            <a>
                <NuxtLink to="/">
                    <button class="btn btn-active text-lg w-full">
                        トップページ
                    </button>
                </NuxtLink>
            </a>
        </div>
    </div>
</template>