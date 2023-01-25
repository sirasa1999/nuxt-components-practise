<template>
    <div class="m-5">
        <div>
            <button class="border bg-gray-200 rounded-lg" @click="menuBar()">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                <path stroke-linecap="round" stroke-linejoin="round" d="M6.75 12a.75.75 0 11-1.5 0 .75.75 0 011.5 0zM12.75 12a.75.75 0 11-1.5 0 .75.75 0 011.5 0zM18.75 12a.75.75 0 11-1.5 0 .75.75 0 011.5 0z" />
                </svg>

            </button>
            <div v-show='menu' class="border">
                <a href="">Edit</a><br/>
                <a href="">Export Data</a><br/>
                <a href="">Delete</a>
            </div>
        </div>
        <div class="pt-6">
            <img src="/">
            <span class="text-xl">Your Full Name </span><br/>
            <span class="text-base text-gray-500">Your Designation</span>
        </div>
        <div class="pt-5">
            <button class="bg-blue-600 text-white p-2 mr-3 rounded-md">Add Friend</button>
            <button class="bg-gray-200 p-2 rounded-md">Message</button>
        </div>
    </div>
</template>

<script lang="ts" setup>
    import { ref } from "vue";
    const menu = ref(false);
    function menuBar(){
        menu.value = !menu.value;
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>