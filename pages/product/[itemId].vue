<template>
    <div :key="renderKey" class="grid grid-cols-12 gap-8 my-16 relative mx-[8%]">
        <div class="col-span-7">
            <nuxt-img :src="data.image" alt="blog-image" format="webp" />
        </div>
        <div class="col-span-5 content-center space-y-8">
            <div v-if="siteType !== 'A' && siteType === 'B' && 200 < itemId && itemId < 300">
                <p class="text-xm font-bold text-red-500">{{ data.darkData }}</p>
            </div>

            <div class="space-y-2">
                <h2 class="text-3xl text-black font-light">{{ data.name }}</h2>
                <p class="text-lg text black">{{ data.summary }}</p>
            </div>

            <h4 class="text-xl text-black">¥ {{ data.price }} (税込)</h4>

            <div v-if="siteType !== 'A' && siteType === 'B' && 100 < itemId && itemId < 200">
                <p class="text-xm font-bold text-red-500">{{ data.darkData }}</p>
            </div>

            <div>
                <div v-if="cartButton">
                    <button class="btn btn-secondary text-lg">カートに追加しました</button>
                </div>
                <div v-else>
                    <div v-if="itemId === 303 && siteType === 'B'">
                        <button onclick="d_modal.showModal()" class="btn btn-neutral text-lg ">カートに追加する</button>
                    </div>
                    <div v-else>
                        <button v-on:click="addCart" class="btn btn-neutral text-lg font-norma">カートに追加する</button>
                    </div>
                </div>
            </div>
        </div>
        <div class="col-span-12 my-16 space-y-8">
            <h2 class="text-3xl">商品説明</h2>
            <div class="text-lg">
                <ContentDoc />
            </div>
        </div>

        <dialog id="d_modal" class="modal">
            <div class="modal-box w-[80%] max-w-3xl p-12">
                <div class="grid grid-cols-subgrid gap-9 col-span-5">
                    <h3 class="col-span-5 text-lg font-bold">こちらの商品を購入するにはアンケートにご協力ください。</h3>
                    <p class="col-span-5 text-lg">1. あなたの性別を教えてください。</p>

                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="radio" name="radio-1" class="radio checked:bg-primary-content" />
                            <span class="label-text text-lg">男性</span>
                        </label>
                    </div>
                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="radio" name="radio-1" class="radio checked:bg-primary-content" />
                            <span class="label-text text-lg">女性</span>
                        </label>
                    </div>
                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="radio" name="radio-1" class="radio checked:bg-primary-content" />
                            <span class="label-text text-lg">その他</span>
                        </label>
                    </div>

                    <p class="col-span-5 text-lg">2. あなたの年齢を教えてください。</p>
                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="radio" name="radio-2" class="radio checked:bg-primary-content" />
                            <span class="label-text text-lg">10代</span>
                        </label>
                    </div>
                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="radio" name="radio-2" class="radio checked:bg-primary-content" />
                            <span class="label-text text-lg">20代</span>
                        </label>
                    </div>
                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="radio" name="radio-2" class="radio checked:bg-primary-content" />
                            <span class="label-text text-lg">30代</span>
                        </label>
                    </div>
                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="radio" name="radio-2" class="radio checked:bg-primary-content" />
                            <span class="label-text text-lg">40代</span>
                        </label>
                    </div>
                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="radio" name="radio-2" class="radio checked:bg-primary-content" />
                            <span class="label-text text-lg">50代</span>
                        </label>
                    </div>
                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="radio" name="radio-2" class="radio checked:bg-primary-content" />
                            <span class="label-text text-lg">60代</span>
                        </label>
                    </div>
                    <div class="form-control col-span-2 pr-32">
                        <label class="label cursor-pointer">
                            <input type="radio" name="radio-2" class="radio checked:bg-primary-content" />
                            <span class="label-text text-lg">70代以上</span>
                        </label>
                    </div>

                    <p class="col-span-5 text-lg">3. この商品をお選びいただいた理由を教えてください。(複数選択可)</p>
                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="checkbox" class="checkbox mr-2" />
                            <span class="label-text text-lg">サイズ</span>
                        </label>
                    </div>
                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="checkbox" class="checkbox" />
                            <span class="label-text text-lg">材質</span>
                        </label>
                    </div>
                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="checkbox" class="checkbox" />
                            <span class="label-text text-lg">色</span>
                        </label>
                    </div>
                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="checkbox" class="checkbox" />
                            <span class="label-text text-lg">価格</span>
                        </label>
                    </div>
                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="checkbox" class="checkbox" />
                            <span class="label-text text-lg">その他</span>
                        </label>
                    </div>
                    <label class="form-control col-span-5 w-full">
                        <div class="label">
                            <span class="label-text">その他を選んだ場合はその理由をお聞かせください。</span>
                        </div>
                        <input type="text" placeholder="その他の理由" class="input input-bordered w-full max-w-xm" />
                    </label>
                </div>
                <div class="modal-action">
                    <form method="dialog">
                        <!-- if there is a button in form, it will close the modal -->
                        <button v-on:click="addCart" class="btn w-32 text-lg">回答する</button>
                    </form>
                </div>
            </div>
        </dialog>
    </div>
</template>

<script setup>
import { ref } from 'vue'
import { useState } from '#app'
import CategoryId from '../category/[categoryId].vue';

const cart = useState('cart')
// const [cart, setCart] = useState([])

const { data } = await useAsyncData(useRoute().path, () =>
    queryContent(useRoute().path).findOne()
)

let cartButton = false

const renderKey = ref(0)

const addCart = () => {
    cart.value.push(data.value)
    cartButton = true
    renderKey.value = renderKey.value + 1

    console.log(cart.value[0].itemId)
}

const siteType = useState('siteType')
const path = useRoute().path
var itemId = Number(path.replace('/product/', ''))
</script>