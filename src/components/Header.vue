<template>
    <header class="bg-white/80 backdrop-blur-lg fixed top-0 left-0 right-0 z-40 border-b border-slate-200">
        <div class="container mx-auto px-6 py-4">
            <div class="flex justify-between items-center">
                <a href="#home" class="text-2xl font-bold text-teal-700">Srijan Ray</a>
                <nav class="hidden md:flex space-x-8">
                    <a href="#about" class="text-slate-600 hover:text-orange-500 transition-colors">About</a>
                    <a href="#experience" class="text-slate-600 hover:text-orange-500 transition-colors">Experience</a>
                    <a href="#projects" class="text-slate-600 hover:text-orange-500 transition-colors">Projects</a>
                    <a href="#publications"
                        class="text-slate-600 hover:text-orange-500 transition-colors">Publications</a>
                    <a href="#skills" class="text-slate-600 hover:text-orange-500 transition-colors">Skills</a>
                    <a href="#contact" class="text-slate-600 hover:text-orange-500 transition-colors">Contact</a>
                </nav>
                <button @click="isOpen = !isOpen" class="md:hidden text-slate-800">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24"
                        stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M4 6h16M4 12h16m-7 6h7" />
                    </svg>
                </button>
            </div>
        </div>
        <!-- Mobile Menu -->
        <div v-if="isOpen" class="md:hidden bg-white border-t border-slate-200">
            <a href="#about" @click="isOpen = false" class="block py-2 px-6 text-slate-600 hover:bg-slate-50">About</a>
            <a href="#experience" @click="isOpen = false"
                class="block py-2 px-6 text-slate-600 hover:bg-slate-50">Experience</a>
            <a href="#projects" @click="isOpen = false"
                class="block py-2 px-6 text-slate-600 hover:bg-slate-50">Projects</a>
            <a href="#publications" @click="isOpen = false"
                class="block py-2 px-6 text-slate-600 hover:bg-slate-50">Publications</a>
            <a href="#skills" @click="isOpen = false"
                class="block py-2 px-6 text-slate-600 hover:bg-slate-50">Skills</a>
            <a href="#contact" @click="isOpen = false"
                class="block py-2 px-6 text-slate-600 hover:bg-slate-50">Contact</a>
        </div>
    </header>
</template>

<script setup>
import { ref } from 'vue';

const isOpen = ref(false);
</script>
