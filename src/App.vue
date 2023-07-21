<script setup>
import { ref } from 'vue'
const light1 = ref('//img.icons8.com/?size=512&id=12244&format=png')
const light2 = ref('//img.icons8.com/?size=512&id=12244&format=png')
const light3 = ref('//img.icons8.com/?size=512&id=12244&format=png')

const button1 = ref('Light 1 On')
const button2 = ref('Light 2 On')
const button3 = ref('Light 3 On')

const isLight1On = ref(true)
const isLight2On = ref(true)
const isLight3On = ref(true)

function light1Function(){
  isLight1On.value == true ? isLight1On.value = false : isLight1On.value = true
  isLight1On.value == true ? button1.value = 'Light 1 On' : button1.value = 'Light 1 OFF'
  isLight1On.value != true ? light1.value = '//img.icons8.com/?size=512&id=75&format=png' : light1.value = '//img.icons8.com/?size=512&id=12244&format=png'
}

function light2Function(){
  isLight2On.value == true ? isLight2On.value = false : isLight2On.value = true
  isLight2On.value == true ? button2.value = 'Light 2 On' : button2.value = 'Light 2 OFF'
  isLight2On.value != true ? light2.value = '//img.icons8.com/?size=512&id=75&format=png' : light2.value = '//img.icons8.com/?size=512&id=12244&format=png'
}

function light3Function(){
  isLight3On.value == true ? isLight3On.value = false : isLight3On.value = true
  isLight3On.value == true ? button3.value = 'Light 3 On' : button3.value = 'Light 3 OFF'
  isLight3On.value != true ? light3.value = '//img.icons8.com/?size=512&id=75&format=png' : light3.value = '//img.icons8.com/?size=512&id=12244&format=png'
}

</script>

<template>
  <section class="container mx-auto flex items-center flex-col">
        <h1 class="text-center text-2xl py-10">Assignment</h1>
        <p class="p-5">Make These Buttons Work</p>
        <div class="flex justify-between space-x-6">
            <div class="p-10 border w-96 flex flex-col space-y-5">
                <button @click="light1Function()" class="text-white font-bold py-2 px-4 rounded" :class="isLight1On == true ? 'bg-blue-500 hover:bg-blue-700' : 'bg-gray-500 hover:bg-gray-700'">
                    {{ button1 }}
                </button>
                <button @click="light2Function()" class="text-white font-bold py-2 px-4 rounded" :class="isLight2On == true ? 'bg-blue-500 hover:bg-blue-700' : 'bg-gray-500 hover:bg-gray-700'">
                  {{ button2 }}
                </button>
                <button @click="light3Function()" class="text-white font-bold py-2 px-4 rounded" :class="isLight3On == true ? 'bg-blue-500 hover:bg-blue-700' : 'bg-gray-500 hover:bg-gray-700'">
                  {{ button3 }}
                </button>
            </div>
            <div class="p-10 border w-96 flex flex-col space-y-5">
                <img class="w-20" :src="light1" alt="">
                <img class="w-20" :src="light2" alt="">
                <img class="w-20" :src="light3" alt="">
            </div>
        </div>
    </section>
</template>

<style scoped></style>