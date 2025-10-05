<template>
  <footer class="bg-slate-100 border-t border-slate-200">
    <div class="container mx-auto px-6 py-8 flex flex-col md:flex-row justify-between items-center text-center md:text-left">
      <div class="mb-4 md:mb-0">
        <p class="text-slate-500">&copy; {{ new Date().getFullYear() }} Srijan Ray. All rights reserved.</p>
      </div>
      <div class="flex space-x-6">
        <a href="https://github.com/StrontiumComputer" target="_blank" class="text-slate-500 hover:text-teal-600 transition-colors duration-300">
          <span class="sr-only">GitHub</span>
          <svg class="w-6 h-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" d="M17.25 6.75L22.5 12l-5.25 5.25m-10.5 0L1.5 12l5.25-5.25m7.5-3l-4.5 16.5" />
          </svg>
        </a>
        <a href="https://www.linkedin.com/in/srijan-ray/" target="_blank" class="text-slate-500 hover:text-teal-600 transition-colors duration-300">
          <span class="sr-only">LinkedIn</span>
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
            <path fill-rule="evenodd" d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" clip-rule="evenodd"/>
          </svg>
        </a>
      </div>
    </div>
  </footer>
</template>

<script setup></script>


