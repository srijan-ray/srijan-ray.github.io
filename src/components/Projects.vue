<template>
  <section id="projects" class="py-20 bg-white">
    <div class="container mx-auto px-6">
      <h2 class="text-4xl font-bold text-center mb-16 text-slate-900">Projects</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div v-for="project in projects" :key="project.title" class="bg-slate-50 rounded-lg shadow-lg overflow-hidden transform hover:-translate-y-2 transition-transform duration-300 border border-slate-200 flex flex-col">
          <img :src="project.imageUrl" alt="Project Image" class="w-full h-48 object-cover">
          <div class="p-6 flex flex-col flex-grow">
            <h3 class="text-2xl font-bold mb-2 text-teal-700">{{ project.title }}</h3>
            <p class="text-slate-600 mb-4 flex-grow">{{ project.description }}</p>
            <div class="mt-auto">
              <button @click="openModal(project)" class="w-full bg-orange-500 text-white font-bold py-2 px-4 rounded-lg hover:bg-orange-600 transition-colors duration-300">
                Learn More
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Modal -->
  <transition name="modal-fade">
    <div v-if="selectedProject" @click.self="closeModal" class="fixed inset-0 bg-black/30 backdrop-blur-sm flex items-center justify-center z-50 p-4">
      <div class="bg-white rounded-xl shadow-2xl max-w-3xl w-full max-h-[90vh] overflow-y-auto">
        <div class="p-8">
          <!-- Modal Header -->
          <div class="flex justify-between items-start mb-4">
            <h2 class="text-3xl font-bold text-slate-800">{{ selectedProject.title }}</h2>
            <button @click="closeModal" class="text-slate-500 hover:text-slate-800">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" /></svg>
            </button>
          </div>
          
          <!-- Tech Stack -->
          <div class="flex flex-wrap gap-2 mb-6">
            <span v-for="tech in selectedProject.technologies" :key="tech" class="bg-teal-100 text-teal-800 text-sm font-semibold px-3 py-1 rounded-full">
              {{ tech }}
            </span>
          </div>
          
          <!-- Video Embed -->
          <div v-if="selectedProject.videoUrl" class="mb-6 rounded-lg overflow-hidden">
            <iframe class="w-full aspect-video" :src="selectedProject.videoUrl" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
          
          <!-- Project Details -->
          <h3 class="text-xl font-bold text-slate-700 mb-3">Project Details</h3>
          <ul class="list-disc list-outside pl-5 text-slate-600 space-y-2 mb-8">
            <li v-for="detail in selectedProject.detailedDescription" :key="detail">{{ detail }}</li>
          </ul>

          <!-- Footer Buttons -->
          <div class="flex justify-end gap-4 border-t pt-6">
            <a v-if="selectedProject.repoUrl" :href="selectedProject.repoUrl" target="_blank" class="bg-slate-700 text-white font-bold py-2 px-6 rounded-lg hover:bg-slate-800 transition-colors duration-300 flex items-center gap-2">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor"><path d="M10 0a10 10 0 00-3.16 19.49c.5.09.68-.22.68-.48v-1.7c-2.78.6-3.37-1.34-3.37-1.34-.45-1.16-1.11-1.47-1.11-1.47-.9-.62.07-.6.07-.6 1 .07 1.53 1.03 1.53 1.03.9 1.52 2.34 1.08 2.91.83.09-.65.35-1.08.63-1.34-2.22-.25-4.55-1.11-4.55-4.94 0-1.1.39-1.99 1.03-2.69a3.6 3.6 0 01.1-2.64s.84-.27 2.75 1.02a9.58 9.58 0 015 0c1.91-1.29 2.75-1.02 2.75-1.02.54 1.3.15 2.34.1 2.64.64.7 1.03 1.6 1.03 2.69 0 3.84-2.34 4.68-4.57 4.93.36.31.68.92.68 1.85v2.74c0 .27.18.58.69.48A10 10 0 0010 0z" /></svg>
              GitHub
            </a>
            <a v-if="selectedProject.liveUrl" :href="selectedProject.liveUrl" target="_blank" class="bg-blue-600 text-white font-bold py-2 px-6 rounded-lg hover:bg-blue-700 transition-colors duration-300 flex items-center gap-2">
               <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M12.586 4.586a2 2 0 112.828 2.828l-3 3a2 2 0 01-2.828 0 1 1 0 00-1.414 1.414 4 4 0 005.656 0l3-3a4 4 0 00-5.656-5.656l-1.5 1.5a1 1 0 101.414 1.414l1.5-1.5zm-5 5a2 2 0 012.828 0 1 1 0 101.414-1.414 4 4 0 00-5.656 0l-3 3a4 4 0 105.656 5.656l1.5-1.5a1 1 0 10-1.414-1.414l-1.5 1.5a2 2 0 11-2.828-2.828l3-3z" clip-rule="evenodd" /></svg>
              Live Demo
            </a>
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>

<style>
.modal-fade-enter-active, .modal-fade-leave-active {
  transition: opacity 0.3s ease;
}
.modal-fade-enter-from, .modal-fade-leave-to {
  opacity: 0;
}
</style>

<script setup>
import { ref } from 'vue';

const selectedProject = ref(null);

const projects = ref([
  {
    title: 'Geographic Spatial Clustering for Observing Provider Equity',
    description: 'A full-stack dashboard for observing equity in the US pharmacy and provider network.',
    imageUrl: 'https://placehold.co/600x400/1d4ed8/ffffff?text=GeoSCOPE',
    technologies: ['Vue.js', 'FastAPI', 'Redis', 'Postgres', 'Docker', 'Leaflet.js'],
    liveUrl: null,
    repoUrl: null,
    videoUrl: null,
    detailedDescription: [
        'Analyzed the entire US Pharmacy and Provider network using data from Palantir Tiberius, US Census Bureau, and Open Street Maps.',
        'Wrote a FastAPI backend to query the Postgres/PostGIS database, using Redis as a cache to accelerate data retrieval from 8 seconds to 2 seconds.',
        'Developed a frontend using Vue 3, Leaflet.js, and TailwindCSS for data visualization to identify neighborhoods at risk during public health emergencies.',
        'Containerized the entire application stack (frontend, backend, database) using Docker for streamlined deployment.'
    ]
  },
  {
    title: 'Note.AI',
    description: 'A web app that uses Generative AI to create multiple-choice questions from user notes.',
    imageUrl: 'https://placehold.co/600x400/f97316/ffffff?text=Note.AI',
    technologies: ['Svelte', 'Django', 'OpenAI API', 'AWS'],
    liveUrl: 'https://devpost.com/software/note-ai#app-team',
    repoUrl: 'https://github.com/srijan-ray/Note.AI',
    videoUrl: 'https://www.youtube.com/embed/kMkXN7oFS-Y?si=9gi-nfI-baFHXvvB',
    detailedDescription: [
        'Created a web app built with Svelte.js and Django to help users study more efficiently by generating quizzes from their notes.',
        'Engineered prompts for the OpenAI API to effectively transform .docx files into structured multiple-choice questions in JSON format.',
        'Designed a Svelte.js frontend to parse the AI-generated JSON and present it in an interactive quiz format.',
        'Assisted in deploying the full-stack application to an AWS EC2 instance.'
    ]
  },
  {
    title: 'Breast Cancer Segmentation',
    description: 'A deep learning model for segmenting breast cancer in PET scans with 98% accuracy.',
    imageUrl: 'https://placehold.co/600x400/10b981/ffffff?text=Deep+Learning',
    technologies: ['Python', 'TensorFlow', 'Keras', 'NumPy', 'OpenCV'],
    liveUrl: null,
    repoUrl: null,
    videoUrl: '',
    detailedDescription: [
        'Designed and built a Convolutional Neural Network (CNN) using TensorFlow and Keras for image segmentation of PET scans.',
        'Developed a data pipeline using NumPy and OpenCV to import and process four large image datasets (over 10,000 images each) from an FTP server.',
        'Trained and evaluated the neural network using K-Fold cross-validation, achieving 98% accuracy based on precision, recall, and f1-score metrics.',
        'Awarded 4th Place in the Math and Computer Science Category at the Regeneron ISEF Regional Science Fair.'
    ]
  }
]);

const openModal = (project) => {
  selectedProject.value = project;
  document.body.style.overflow = 'hidden'; // Prevent background scrolling
};

const closeModal = () => {
  selectedProject.value = null;
  document.body.style.overflow = ''; // Restore scrolling
};

// Add keyboard listener to close modal with Escape key
import { onMounted, onUnmounted } from 'vue';
const handleKeydown = (e) => {
  if (e.key === 'Escape' && selectedProject.value) {
    closeModal();
  }
};
onMounted(() => window.addEventListener('keydown', handleKeydown));
onUnmounted(() => window.removeEventListener('keydown', handleKeydown));

</script>
