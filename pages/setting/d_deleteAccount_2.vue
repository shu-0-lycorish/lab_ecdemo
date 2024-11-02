<template>
    dark_deleteAccount_2
    <div class="grid grid-cols-12 gap-8 my-16 pb-[6%] relative mx-[8%]">
        <div class="col-span-12">
            <h1 class="text-4xl">退会</h1>
        </div>
        <div class="col-span-12 py-14">
            <div class="flex flex-col space-y-4">

                <h3 class="text-2xl">退会によるデータ削除と再登録時の注意点</h3>
                <p class="text-lg">
                    一度退会されますと、お客様のデータ、ポイント、特典、利用履歴は全て無効となり、再登録を行った際も復元することができません。
                    また、会員の皆様にとって特典となる長年の利用に応じたリワードも消失してしまいますので、ぜひ再加入プランについてご検討いただければと思います。
                </p>

                <div class="col-span-12 flex-1 border-b border-gray-500"></div>

                <h3 class="text-2xl">その他特別なオファーとキャンペーンのご案内</h3>
                <p class="text-lg">
                    退会手続きの前に、当サービスがご提供する特別なオファーやキャンペーンをもう一度ご確認いただければと思います。
                    これらのキャンペーンは期間限定で行われており、会員様のみにご利用いただける特典が多数ございます。
                    また、退会を検討されているお客様のために、特別に割引価格での再加入も可能となっておりますので、ぜひこの機会にご利用ください。
                </p>

                <div class="col-span-12 flex-1 border-b border-gray-500"></div>

                <h3 class="text-2xl">アンケートのお願い</h3>
                <p class="text-lg">
                    私たちは、サービスを日々進化させるために、会員様からのフィードバックをとても大切にしています。
                    お客様が退会に至るご決断をされた背景やお考えを伺い、今後のサービス改善に役立てたいと考えております。
                    以下に簡単なアンケートをご用意いたしましたので、ぜひご協力をお願い申し上げます。
                </p>

                <div class="grid grid-cols-subgrid gap-16 col-span-8">
                    <p class="col-span-5 text-lg">退会の理由を教えてください。(複数選択可)</p>
                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="checkbox" class="checkbox" />
                            <span class="label-text text-lg">商品の充実度</span>
                        </label>
                    </div>
                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="checkbox" class="checkbox" />
                            <span class="label-text text-lg">商品の質</span>
                        </label>
                    </div>
                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="checkbox" class="checkbox" />
                            <span class="label-text text-lg">商品の価格</span>
                        </label>
                    </div>
                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="checkbox" class="checkbox" />
                            <span class="label-text text-lg">お届け日数</span>
                        </label>
                    </div>
                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="checkbox" class="checkbox" />
                            <span class="label-text text-lg">お客様への対応</span>
                        </label>
                    </div>
                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="checkbox" class="checkbox mr-2" />
                            <span class="label-text text-lg">サイトの操作性</span>
                        </label>
                    </div>
                    <div class="form-control">
                        <label class="label cursor-pointer">
                            <input type="checkbox" class="checkbox" />
                            <span class="label-text text-lg">その他</span>
                        </label>
                    </div>
                    <label class="form-control col-span-5 w-full">
                        <p class="text-lg">退会理由を詳しくお書きください。</p>
                        <textarea class="textarea textarea-bordered text-xl w-full h-80"></textarea>
                    </label>
                </div>

                <p class="text-lg">
                    アンケートにご回答いただきました後、<NuxtLink to="/setting/d_deleteAccount_3" class="underline hover:text-blue-500">次のページ
                    </NuxtLink>で退会手続きを続けることが可能です。再度のご確認をお願い申し上げます。
                </p>
            </div>
        </div>

        <div class="col-start-6 col-span-2">
            <a>
                <NuxtLink to="/setting/account">
                    <button class="btn btn-active text-lg w-full">退会せずに戻る</button>
                </NuxtLink>
            </a>
        </div>
    </div>
</template>