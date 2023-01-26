<template>
    <div class="p-2 m-5 border w-96 h-64 rounded-lg relative">
            <button class="border bg-gray-200 rounded-lg float-right" @click="menuBar()">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                <path stroke-linecap="round" stroke-linejoin="round" d="M6.75 12a.75.75 0 11-1.5 0 .75.75 0 011.5 0zM12.75 12a.75.75 0 11-1.5 0 .75.75 0 011.5 0zM18.75 12a.75.75 0 11-1.5 0 .75.75 0 011.5 0z" />
                </svg>

            </button>
            <div v-show='menu' class="border my-7 w-32 absolute right-2 p-2">
                <a href="e">Edit</a><br/>
                <a href="ed">Export Data</a><br/>
                <a href="" class='text-red-500'>Delete</a>
            </div>
        <div class='grid place-items-center text-center p-2'>
            <div class="pt-6">
                <img class="rounded-full h-20 w-20 m-auto" src="https://picsum.photos/id/237/200/300" alt="hello"/>
                <span class="text-xl">Your Full Name </span><br/>
                <span class="text-base text-gray-500">Your Designation</span>
            </div>
            <div class="pt-5">
                <button class="bg-blue-600 text-white p-2 mr-3 rounded-md">Add Friend</button>
                <button class="bg-gray-200 p-2 rounded-md">Message</button>
            </div>
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