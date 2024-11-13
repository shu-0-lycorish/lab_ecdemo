<template>
    <div class="grid grid-cols-12 gap-8 my-16 pb-[6%] relative mx-[8%]">
        <div class="col-span-12">
            <h1 class="text-4xl">退会</h1>
        </div>
        <div class="col-span-12 py-14">
            <div class="flex flex-col space-y-4">
                <h3 class="text-2xl">退会をご決断される前に再度のご確認をお願いいたします</h3>
                <p class="text-lg">
                    最後に、本当に退会されるご決心であるかを再確認していただけますと幸いです。
                    お客様がこれまで積み重ねられたご利用履歴、ポイント、特典の数々は一度退会手続きが完了すると全て消失し、再登録を行った際にも引き継ぐことができません。
                    今後の新しいサービスや更新される特典をご利用いただけない形となりますので、ぜひ今一度ご検討ください。
                </p>

                <div class="col-span-12 flex-1 border-b border-gray-500"></div>

                <h3 class="text-2xl">再加入には一定のクールダウン期間が必要です</h3>
                <p class="text-lg">
                    一度退会されると、再加入の際には一定期間のクールダウン期間が適用されます。
                    この期間中は再登録いただいた場合にも一部のサービスが制限され、以前のようにスムーズにご利用いただけない可能性がございます。
                </p>

                <div class="col-span-12 flex-1 border-b border-gray-500"></div>

                <h3 class="text-2xl">サポートセンターでのご相談をお待ちしております</h3>
                <p class="text-lg">
                    私たちのサポートセンターでは、退会をお考えのお客様に対して、あらゆるサポートをご提供しております。
                    退会に関するお悩みやご不安、ご不明点がございましたら、24時間体制でお客様のご相談に対応しておりますので、どうぞお気軽にお問い合わせください。
                    豊富な経験を持つスタッフが親身にサポートし、最適なアドバイスを提供いたします。
                </p>

                <p class="text-lg">
                    このページの内容をご確認いただき、<NuxtLink to="/setting/compDeleteAccount" class="underline hover:text-blue-500">こちら</NuxtLink>で手続きを完了されますと、お客様のアカウントは削除され、データの復元はできなくなります。
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