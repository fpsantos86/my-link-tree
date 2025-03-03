<template>  
    <div class="pt-6 text-center space-y-4">
      <a v-if="link" :href="link" target="_blank"
         class="flex rounded-lg border border-gray-400 bg-white px-5 py-4 text-lg leading-6 font-medium shadow-md hover:shadow-xl transition ease-in-out duration-150">
        <p class="mr-3 h-6 w-6">{{ icon }}</p>
        {{ text }}
        <div class="ml-auto mt-0.5 pl-4">
          <svg class="h-5 w-5 text-gray-400" xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 20 20">
            <path fill-rule="evenodd" d="M4.646 1.646a.5.5 0 0 1 .708 0l6 6a.5.5 0 0 1 0 .708l-6 6a.5.5 0 0 1-.708-.708L10.293 8 4.646 2.354a.5.5 0 0 1 0-.708z" />
          </svg>
        </div>
      </a>
  
      <!-- Caso não tenha link, cria um botão clicável -->
      <button v-else @click="emitirEvento"
         class="flex w-full rounded-lg border border-gray-400 bg-white px-5 py-4 text-lg leading-6 font-medium shadow-md hover:shadow-xl transition ease-in-out duration-150">
        <p class="mr-3 h-6 w-6">{{ icon }}</p>
        {{ text }}
        <div class="ml-auto mt-0.5 pl-4">
          <svg class="h-5 w-5 text-gray-400" xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 20 20">
            <path fill-rule="evenodd" d="M4.646 1.646a.5.5 0 0 1 .708 0l6 6a.5.5 0 0 1 0 .708l-6 6a.5.5 0 0 1-.708-.708L10.293 8 4.646 2.354a.5.5 0 0 1 0-.708z" />
          </svg>
        </div>
      </button>
    </div>
  </template>
  
  <script setup>
  const { link, icon, text } = defineProps(['link', 'icon', 'text']);
  const emit = defineEmits(['click']); // Permite que o componente emita eventos
  
  const emitirEvento = () => {
    emit('click'); // Emite o evento quando clicado
  };
  </script>
  