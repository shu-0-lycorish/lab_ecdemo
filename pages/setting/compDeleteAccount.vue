<template>
    <div class="grid grid-cols-12 gap-8 my-16 pb-[6%] relative mx-[8%]">
        <div class="col-span-12">
            <h1 class="text-4xl">退会手続き完了</h1>
        </div>
        <div class="col-span-12 py-14">
            <div class="flex flex-col space-y-4">
                <p class="text-lg">
                    退会手続きが完了しました。
                </p>
                <p class="text-lg">
                    会員限定の割引やセール、ポイントプログラムなどの特典は、退会後にはご利用いただけません。
                    また、これまで貯めていただいたポイントは、退会と同時に失効いたしますのでご了承ください。
                </p>
                <p class="text-lg">
                    これまでご愛顧いただき、心より感謝申し上げます。
                    スタッフ一同、またお会いできることを心からお待ちしております。
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