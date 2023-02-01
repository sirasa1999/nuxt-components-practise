<template>
    <div @click='showInfo()'>
    <img class="h-10 w-10 border border-gray-600 rounded-full cursor-pointer" src="https://picsum.photos/seed/picsum/200/300" alt="happy" />
    </div>
    <div v-show='info' class='border rounded-xl w-1/5 ml-5 p-1'>
        <div>
        <h4>Your Name</h4>
        <h4>your@email.com</h4>
        </div>
        <hr/>
        <div>
        <a href='#'>Dashboard</a><br/>
        <a href='#'>Settings</a><br/>
        <a href='#'>Earnings</a>
        </div>
        <hr/>
        <div>
        <a href='#'>Sign out</a>
        </div>
    </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";
let info = ref(false);
function showInfo(){
    info.value = !info.value
}
</script>