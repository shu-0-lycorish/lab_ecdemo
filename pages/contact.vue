<template>
    <div class="grid grid-cols-12 gap-8 mx-[8%] my-16">
        <div class="col-span-12">
            <h1 class="text-4xl">お問い合わせ</h1>
        </div>

        <div class="grid grid-cols-subgrid gap-8 col-span-12 py-8 flex items-center">
            <div class="col-start-3 col-span-4">
                <label class="input input-bordered flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="currentColor"
                        class="h-4 w-4 opacity-70">
                        <path
                            d="M8 8a3 3 0 1 0 0-6 3 3 0 0 0 0 6ZM12.735 14c.618 0 1.093-.561.872-1.139a6.002 6.002 0 0 0-11.215 0c-.22.578.254 1.139.872 1.139h9.47Z" />
                    </svg>
                    <input type="text" class="grow text-xl" placeholder="お名前" />
                </label>
            </div>

            <div class="col-end-11 col-span-4">
                <label class="input input-bordered flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="currentColor"
                        class="h-4 w-4 opacity-70">
                        <path
                            d="M2.5 3A1.5 1.5 0 0 0 1 4.5v.793c.026.009.051.02.076.032L7.674 8.51c.206.1.446.1.652 0l6.598-3.185A.755.755 0 0 1 15 5.293V4.5A1.5 1.5 0 0 0 13.5 3h-11Z" />
                        <path
                            d="M15 6.954 8.978 9.86a2.25 2.25 0 0 1-1.956 0L1 6.954V11.5A1.5 1.5 0 0 0 2.5 13h11a1.5 1.5 0 0 0 1.5-1.5V6.954Z" />
                    </svg>
                    <input type="text" class="grow text-xl" placeholder="メールアドレス" />
                </label>
            </div>

            <div class="col-start-3 col-span-8">
                <textarea class="textarea textarea-bordered text-xl w-full h-80"
                    placeholder="お問い合わせの内容を詳しくお書きください。"></textarea>
            </div>

            <div class="col-start-6 col-span-2">
                <button class="btn btn-primary text-lg w-full">送信する</button>
            </div>
        </div>
    </div>
</template>