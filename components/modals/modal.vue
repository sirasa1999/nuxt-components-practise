<template>
  <div class="flex justify-center">
    <button v-show="modalButton" @click="Toggle()" class="bg-blue-800 text-white border p-2 rounded-xl">
      Toggle modal
    </button>
    <div v-show='modal' class=' bg-black bg-opacity-60 flex justify-center'>
      <div class="p-5 m-2 bg-white text-left w-3/5 border">
        <div class='flex justify-between items-center'>
          <h3 class="font-bold p-2">Static Modal</h3>
          <button @click="Toggle()" class=''><svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-6 h-6"
            >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M6 18L18 6M6 6l12 12"
            />
          </svg>
          </button>
      </div>
      <hr />
      <p class="p-2">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
        velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint
        occaecat cupidatat non proident, sunt in culpa qui officia deserunt
        mollit anim id est laborum.
        <br />
        <ul v-for="name in names">
        <!-- v-if="name[0]=='S'" -->
        <li>
            {{ name }}
        </li>
        </ul>
        Ted ut perspiciatis unde omnis iste natus error sit voluptatem
        accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab
        illo inventore veritatis et quasi architecto beatae vitae dicta sunt
        explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut
        odit aut fugit, sed quia consequuntur magni dolores eos qui ratione
        voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum
        quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam
        eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat
        voluptatem.
      </p>
      <hr />
      <div class="p-2">
        <button class="bg-blue-800 text-white border p-2 mr-3 rounded-xl">
          I Accept
        </button>
        <button class="text-gray-600 border p-2 rounded-xl">Decline</button>
      </div>
    </div>
  </div>
</div>  
</template>

<script lang="ts" setup>
    import { ref } from "vue";
    const modalButton = ref(true);
    const modal = ref(false);
    
    function Toggle() {
    modal.value = !modal.value;
    modalButton.value = !modalButton.value;
    }
    let names = ['Sirasa', 'Salina', 'Likhita', 'Binita', 'Supiya', 'Bipana', 'Nirmala']
</script>