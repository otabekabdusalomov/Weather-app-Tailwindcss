<template>
    <header class="sticky top-0 bg-weather-primary shadow-lg">
        <div class="container flex flex-col sm:flex-row items-center gap-4 text-white py-6">
            <RouterLink :to="{ name: 'main' }">
                <div class="flex items-center gap-3">
                <i class="fa-solid fa-sun text-2xl"></i>
                <p class="text-2xl">The Local Weather</p>
            </div>
            </RouterLink>

           <div class="flex gap-3 flex-1 justify-end">
            <i class="fa-solid fa-circle-info text-xl hover:text-weather-secondary duration-150 cursor-pointer" @click="toggleModal"></i>
            <i class="fa-solid fa-plus text-xl hover:text-weather-secondary duration-150 cursor-pointer"></i>
           </div> 

           <BaseModal :modalActive="modalActive" @close-modal="toggleModal">
             <div class="text-black">
                <h1 class="text-2xl mb-1">About:</h1>
                <p class="mb-4">The Local Weather allows you to track the current and future wether of cities of your chhosing</p>
                <h2 class="text-2xl">How it works:</h2>
                <ol class="list-decimal list-inside mb-4">
                    <li>Search for your city by entering the nema into the search bar.</li>
                    <li>Search for your city by entering the nema into the search bar.</li>
                    <li>Search for your city by entering the nema into the search bar.</li>
                </ol>

                <h2 class="text-2xl">Removing a city</h2>
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Placeat ab nulla nihil explicabo ad aspernatur? Molestias iusto saepe hic provident. Voluptatem quasi eos delectus dolorum.</p>
             </div>
           </BaseModal>
        </div>
    </header>
</template>

<script setup>
import { ref } from "vue";
import { RouterLink } from 'vue-router';
import BaseModal from "./BaseModal.vue";

const modalActive = ref(null);
const toggleModal = () => {
    modalActive.value = !modalActive.value;
};
</script>
