<template>
  <section id="about" class="py-20 bg-white">
    <div class="container mx-auto px-6">
      <h2 class="text-4xl font-bold text-center mb-6 text-slate-900">About Me</h2>
      
      <!-- Summary Blurb -->
      <div class="max-w-4xl mx-auto text-center mb-12">
        <p class="text-slate-600 text-lg leading-relaxed bg-white p-6 rounded-lg shadow-sm border border-slate-200">
          I am a passionate and driven Computer Science student at the <strong class="font-semibold text-teal-700">Georgia Institute of Technology</strong>, specializing in Artificial Intelligence and Modeling & Simulation. My goal is to leverage technology to build innovative AI-driven solutions that solve real-world problems. I thrive in environments where I can tackle complex challenges, from developing full-stack applications to designing and training deep learning models.
        </p>
      </div>

      <!-- Education and Coursework Grid -->
      <div class="max-w-5xl mx-auto grid lg:grid-cols-5 gap-8">
        
        <!-- Education Card (Spans 2 columns) -->
        <div class="lg:col-span-2 bg-white p-6 rounded-lg shadow-lg border border-slate-200">
          <h3 class="text-2xl font-bold mb-6 text-slate-800 flex items-center">
            <span class="flex-shrink-0 w-10 h-10 bg-blue-100 text-blue-600 rounded-full flex items-center justify-center mr-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path d="M12 14l9-5-9-5-9 5 9 5z" />
                <path d="M12 14l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-5.998 12.078 12.078 0 01.665-6.479L12 14z" />
                <path stroke-linecap="round" stroke-linejoin="round" d="M12 14l9-5-9-5-9 5 9 5zm0 0l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-5.998 12.078 12.078 0 01.665-6.479L12 14zm-4 6v-7.5l4-2.222" />
              </svg>
            </span>
            Education
          </h3>
          <div class="space-y-4 text-slate-700">
            <p class="text-xl font-semibold text-teal-600">Georgia Institute of Technology</p>
            <p>Bachelor of Science in Computer Science</p>
            <p class="text-sm text-slate-500">Concentrations: AI & Modeling/Simulation</p>
            <div class="border-t border-slate-200 my-4"></div>
            <div class="flex items-center text-sm">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2 text-slate-400" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" /></svg>
                <span>GPA: 3.86 / 4.0</span>
            </div>
             <div class="flex items-center text-sm">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2 text-slate-400" viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M6 2a1 1 0 00-1 1v1H4a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V6a2 2 0 00-2-2h-1V3a1 1 0 10-2 0v1H7V3a1 1 0 00-1-1zm0 5a1 1 0 000 2h8a1 1 0 100-2H6z" clip-rule="evenodd" /></svg>
                <span>Aug 2023 - May 2027 (Expected)</span>
            </div>
            <div class="flex items-center text-sm">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2 text-slate-400" viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd" /></svg>
              <span>Atlanta, GA</span>
            </div>
          </div>
        </div>

        <!-- Coursework Card (Spans 3 columns) -->
        <div class="lg:col-span-3 bg-white p-6 rounded-lg shadow-lg border border-slate-200">
          <h3 class="text-2xl font-bold mb-6 text-slate-800">Key Coursework</h3>
          <div class="flex flex-wrap gap-3">
              <span class="bg-teal-100 text-teal-800 font-semibold px-4 py-2 rounded-md">Machine Learning</span>
              <span class="bg-teal-100 text-teal-800 font-semibold px-4 py-2 rounded-md">Computer Vision</span>
              <span class="bg-teal-100 text-teal-800 font-semibold px-4 py-2 rounded-md">Artificial Intelligence</span>
              <span class="bg-teal-100 text-teal-800 font-semibold px-4 py-2 rounded-md">Design & Analysis of Algorithms</span>
                        <span class="bg-teal-100 text-teal-800 font-semibold px-4 py-2 rounded-md">Data Structures & Algorithms</span>
              <span class="bg-teal-100 text-teal-800 font-semibold px-4 py-2 rounded-md">Operating Systems and Networks</span>
                        <span class="bg-teal-100 text-teal-800 font-semibold px-4 py-2 rounded-md">Probability & Statistics</span>
              <span class="bg-teal-100 text-teal-800 font-semibold px-4 py-2 rounded-md">Computer Organization & Programming</span>
              <span class="bg-teal-100 text-teal-800 font-semibold px-4 py-2 rounded-md">Linear Algebra</span>
              <span class="bg-teal-100 text-teal-800 font-semibold px-4 py-2 rounded-md">Multivariable Calculus</span>
              <span class="bg-slate-200 text-slate-700 font-semibold px-4 py-2 rounded-md">and more...</span>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
</script>
