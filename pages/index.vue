<template>
    <div class="grid grid-cols-12 gap-8 mx-[8%] my-16">
        <div class="col-span-12">
            <h1 class="text-4xl">実験情報の入力</h1>
        </div>

        <div class="col-span-12">
            <h4 class="text-xl">
                テキストボックスに指示された内容を入力してください．
                <br>
                入力完了後，「実験を開始する」のボタンから実験を開始してください．
            </h4>
            <p class="text-lg text-red-500">(※半角英数字で入力)</p>
        </div>

        <div class="col-start-5 col-span-4 flex justify-center items-end">
            <p>実験No:　</p>
            <div v-if="siteTypeInput === '' && subjectIDInput === ''">
                <h1 class="text-4xl text-primary">????</h1>
            </div>
            <div v-if="siteTypeInput === '' && subjectIDInput !== ''">
                <h1 class="text-4xl text-primary">{{ "?" + subjectIDInput }}</h1>
            </div>
            <div v-if="siteTypeInput !== '' && subjectIDInput === ''">
                <h1 class="text-4xl text-primary">{{ siteTypeInput + "???" }}</h1>
            </div>
            <div v-if="siteTypeInput !== '' && subjectIDInput !== ''">
                <h1 class="text-4xl text-primary">{{ siteTypeInput + subjectIDInput }}</h1>
            </div>
        </div>

        <div class="grid grid-cols-subgrid gap-8 col-span-12 py-8 flex items-center">
            <div class="col-start-5 col-span-4">
                <label class="input input-bordered flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor"
                        class="h-8 w-8 opacity-70">
                        <path
                            d="M8.749,9.934c0,0.247-0.202,0.449-0.449,0.449H4.257c-0.247,0-0.449-0.202-0.449-0.449S4.01,9.484,4.257,9.484H8.3C8.547,9.484,8.749,9.687,8.749,9.934 M7.402,12.627H4.257c-0.247,0-0.449,0.202-0.449,0.449s0.202,0.449,0.449,0.449h3.145c0.247,0,0.449-0.202,0.449-0.449S7.648,12.627,7.402,12.627 M8.3,6.339H4.257c-0.247,0-0.449,0.202-0.449,0.449c0,0.247,0.202,0.449,0.449,0.449H8.3c0.247,0,0.449-0.202,0.449-0.449C8.749,6.541,8.547,6.339,8.3,6.339 M18.631,4.543v10.78c0,0.248-0.202,0.45-0.449,0.45H2.011c-0.247,0-0.449-0.202-0.449-0.45V4.543c0-0.247,0.202-0.449,0.449-0.449h16.17C18.429,4.094,18.631,4.296,18.631,4.543 M17.732,4.993H2.46v9.882h15.272V4.993z M16.371,13.078c0,0.247-0.202,0.449-0.449,0.449H9.646c-0.247,0-0.449-0.202-0.449-0.449c0-1.479,0.883-2.747,2.162-3.299c-0.434-0.418-0.714-1.008-0.714-1.642c0-1.197,0.997-2.246,2.133-2.246s2.134,1.049,2.134,2.246c0,0.634-0.28,1.224-0.714,1.642C15.475,10.331,16.371,11.6,16.371,13.078M11.542,8.137c0,0.622,0.539,1.348,1.235,1.348s1.235-0.726,1.235-1.348c0-0.622-0.539-1.348-1.235-1.348S11.542,7.515,11.542,8.137 M15.435,12.629c-0.214-1.273-1.323-2.246-2.657-2.246s-2.431,0.973-2.644,2.246H15.435z">
                        </path>
                    </svg>
                    <input type="text" v-model="subjectIDInput" class="grow text-xl" placeholder="被験者ID" />
                </label>
            </div>

            <div class="col-start-5 col-span-4">
                <label class="input input-bordered flex items-center gap-2">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor"
                        class="h-8 w-8 opacity-70">
                        <path
                            d="M17.35,2.219h-5.934c-0.115,0-0.225,0.045-0.307,0.128l-8.762,8.762c-0.171,0.168-0.171,0.443,0,0.611l5.933,5.934c0.167,0.171,0.443,0.169,0.612,0l8.762-8.763c0.083-0.083,0.128-0.192,0.128-0.307V2.651C17.781,2.414,17.587,2.219,17.35,2.219M16.916,8.405l-8.332,8.332l-5.321-5.321l8.333-8.332h5.32V8.405z M13.891,4.367c-0.957,0-1.729,0.772-1.729,1.729c0,0.957,0.771,1.729,1.729,1.729s1.729-0.772,1.729-1.729C15.619,5.14,14.848,4.367,13.891,4.367 M14.502,6.708c-0.326,0.326-0.896,0.326-1.223,0c-0.338-0.342-0.338-0.882,0-1.224c0.342-0.337,0.881-0.337,1.223,0C14.84,5.826,14.84,6.366,14.502,6.708">
                        </path>
                    </svg>
                    <input type="text" v-model="siteTypeInput" class="grow text-xl" placeholder="実験種別" />
                </label>
            </div>

            <div class="col-start-6 col-span-2">
                <NuxtLink to="/top"><button v-on:click="startExpt" class="btn btn-primary text-lg w-full">実験を開始する</button></NuxtLink>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'
import { useState } from '#app'

const subjectIDInput = ref('')
const siteTypeInput = ref('')

const subjectID = useState('subjectID')
const siteType = useState('siteType')

const startExpt = () => {
    subjectID.value = subjectIDInput
    siteType.value = siteTypeInput

    console.log(subjectID.value)
    console.log(siteType.value)
    console.log("start expt")
}
</script>