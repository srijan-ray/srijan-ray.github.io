<template>
  <section id="experience" class="py-20 bg-slate-50">
    <div class="container mx-auto px-6">
      <h2 class="text-4xl font-bold text-center mb-16 text-slate-900">Work Experience</h2>
      <!-- Increased max-width for a wider layout -->
      <div class="relative max-w-5xl mx-auto">
        <!-- Moved timeline further to the left -->
        <div class="absolute left-2 top-1 w-0.5 h-full bg-slate-200"></div>

        <!-- Timeline Items -->
        <div 
          v-for="job in experiences" 
          :key="job.company" 
          class="relative pl-16 pb-12"
        >
          <!-- Adjusted circle position to match the line -->
          <div class="absolute left-2 top-1 w-4 h-4 bg-white border-2 border-orange-500 rounded-full -translate-x-1/2"></div>

          <!-- Timeline Card -->
          <div class="bg-white p-6 rounded-lg shadow-lg border border-slate-200 transform hover:-translate-y-1 transition-transform duration-300">
            <div class="flex flex-col sm:flex-row">
              <!-- Left Side: Role Info -->
              <div class="sm:w-2/5 pr-4 mb-4 sm:mb-0">
                <div class="flex items-center mb-4">
                   <span class="flex-shrink-0 w-12 h-12 bg-blue-100 text-blue-600 rounded-full flex items-center justify-center mr-4">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                      <path stroke-linecap="round" stroke-linejoin="round" d="M21 13.255A23.931 23.931 0 0112 15c-3.183 0-6.22-.62-9-1.745M16 6V4a2 2 0 00-2-2h-4a2 2 0 00-2 2v2m4 6h.01M5 20h14a2 2 0 002-2V8a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                    </svg>
                  </span>
                  <div>
                    <h3 class="text-xl font-bold text-teal-700">{{ job.role }}</h3>
                    <p class="text-md font-semibold text-slate-600">{{ job.company }}</p>
                  </div>
                </div>
                 <div class="flex items-center text-sm text-slate-500 mb-2">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 mr-2" viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd" /></svg>
                  {{ job.location }}
                </div>
                <div class="flex items-center text-sm text-slate-500">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 mr-2" viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M6 2a1 1 0 00-1 1v1H4a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V6a2 2 0 00-2-2h-1V3a1 1 0 10-2 0v1H7V3a1 1 0 00-1-1zm0 5a1 1 0 000 2h8a1 1 0 100-2H6z" clip-rule="evenodd" /></svg>
                  {{ job.duration }}
                </div>
              </div>
              
              <!-- Right Side: Achievements & Tech -->
              <div class="sm:w-3/5 sm:border-l sm:pl-4 border-slate-200">
                <h4 class="font-bold text-slate-800 mb-2">Key Achievements</h4>
                <!-- Switched to list-outside and added pl-5 for proper hanging indent -->
                <ul class="list-disc list-outside pl-5 text-slate-600 space-y-1 mb-4">
                  <li v-for="desc in job.description" :key="desc">{{ desc }}</li>
                </ul>

                <h4 class="font-bold text-slate-800 mb-2">Technologies Used</h4>
                <div class="flex flex-wrap gap-2">
                   <span v-for="tech in job.technologies" :key="tech" class="bg-teal-100 text-teal-800 text-xs font-semibold px-3 py-1 rounded-full">
                     {{ tech }}
                   </span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const experiences = [
  {
    role: 'Software Engineering Intern',
    company: 'JHU Applied Physics Laboratory',
    location: 'Laurel, MD',
    duration: 'May 2025 - Present',
    description: [
      'Developed new feature enhancing LLM generated messages and upgraded application web interface using Vue.JS and Python, enabling more targeted and emotional messaging and overall easier to use user interface',
      'Engineered web dashboard for monitoring usage statistics and dataset availability using Vue.JS and FastAPI, streamlining usage metrics tracking, increasing ease of use for operators, and providing real-time monitoring of usage data',
      'Created platform for evaluating various open-source LLMs on use-case specific benchmarks (GPQA, MMLU, etc.) using Vue.JS and ElasticSearch, benchmarking nearly 5000 open-source LLMs on 50+ metrics'
    ],
    technologies: ['Vue.js', 'Python', 'FastAPI', 'ElasticSearch']
  },
  {
    role: 'ML Research Assistant',
    company: 'Georgia Tech / Emory University',
    location: 'Atlanta, GA',
    duration: 'October 2024 - Present',
    description: [
      'Designing novel technique for training deep learning models for biomedical image analysis using TensorFlow, NumPy, potentially cutting down days to weeks of time spent manually labelling images for image segmentation',
      'Exploring unsupervised/supervised clustering techniques for biomedical data analysis of 200,000+ cell nuceli',
      'Published a peer-reviewed paper in ACS Omega using binary segmentation and dynamic programming step-detection algorithms for detecting ligand binding to virions'
    ],
    technologies: ['TensorFlow', 'NumPy', 'Python', 'Deep Learning']
  },
  {
    role: 'AI/Machine Learning Intern',
    company: 'JHU Applied Physics Laboratory',
    location: 'Laurel, MD',
    duration: 'May 2024 - May 2025',
    description: [
      'Developed a full-stack dashboard (Vue.JS, FastAPI, PostgreSQL) for an HHS project, enabling the efficient coordination and distribution of therapeutic products across the United States, processing and analyzing more than 5 million datapoints',
      'Engineered a streamlined command system in Kotlin and JavaFX for an AI modeling tool, increasing compatibility with diverse LLMs (e.g., Llama, GPT-4) and simplifying user workflows',
      'Awarded Special Achievement Award for Outstanding Dedication and Positive Influence and Technical Expertise (Only given to 1 out of 100 interns)'
    ],
    technologies: ['Vue.js', 'FastAPI', 'PostgreSQL', 'Kotlin', 'JavaFX']
  }
];
</script>


