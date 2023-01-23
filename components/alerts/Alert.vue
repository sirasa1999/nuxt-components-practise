<template>
    <div v-show="showAlert" v-if="alertBox" class="border-4 border-teal-400 border-t-8 border-teal-600 p-5 m-5 flex flex-row w-1/2 delay-1000">
        <div class="bg-white text-teal-500 mr-1">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M11.25 11.25l.041-.02a.75.75 0 011.063.852l-.708 2.836a.75.75 0 001.063.853l.041-.021M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-9-3.75h.008v.008H12V8.25z" />
            </svg>
        </div>
        <div class="px-1 text-teal-400">
            <p>A simple info alert with an <a href="#" class="underline underline-offset-1">example link.</a> Give it a click if you like.</p>
        </div>
        <div class="bg-white text-teal-400 ml-1">
        <button @click="Toggle()" class="">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M9.75 9.75l4.5 4.5m0-4.5l-4.5 4.5M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
        </button>
        </div>
    </div>
    <br/>
    <button v-show='button' @click="Toggle()"  class="border-2 border-purple-900 p-2 ml-5 animate-bounce">Click here!!!</button>
</template>

<script lang="ts" setup>
import { ref } from "vue";
const showAlert = ref(false);
const button = ref(true);
const alertBox = ref(true)
function Toggle() {
  showAlert.value = !showAlert.value;
  button.value = !button.value;
}setTimeout(() => alertBox.value = false, 5000);
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>