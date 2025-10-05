<template>
  <section id="publications" class="py-20 bg-slate-50">
    <div class="container mx-auto px-6">
      <h2 class="text-4xl font-bold text-center mb-16 text-slate-900">Publications</h2>
      <div class="max-w-4xl mx-auto space-y-8">
        
        <div v-for="pub in publications" :key="pub.title" class="bg-white p-6 rounded-lg shadow-lg border border-slate-200 transform hover:-translate-y-1 transition-transform duration-300">
          <h3 class="text-xl font-bold text-teal-700 mb-2">{{ pub.title }}</h3>
          <p class="text-slate-600 mb-3" v-html="pub.authors"></p>
          <div class="text-sm text-slate-500 mb-4">
            <span class="italic">{{ pub.journal }}</span>
            <span v-if="pub.volume">, vol. {{ pub.volume }}</span>
            <span v-if="pub.number">, no. {{ pub.number }}</span>
            <span v-if="pub.pages">, pp. {{ pub.pages }}</span>
            <span>, {{ pub.year }}</span>
          </div>
          <a :href="pub.doiUrl" target="_blank" class="inline-block bg-blue-600 text-white font-bold py-2 px-4 rounded-lg hover:bg-blue-700 transition-colors duration-300 text-sm">
            View Publication
          </a>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
const publications = [
  {
    title: 'ACE2 Receptor and Antibody Binding to SARS-CoV-2 Spikes and Virions by Single-Molecule Fluorescence',
    authors: 'Dasgupta, Souradip, <strong>Ray, Srijan</strong>, Srivatsav, Aswin T., DeVico, Anthony L., and Ray, Krishanu',
    journal: 'ACS Omega',
    volume: '10',
    number: '31',
    pages: '34844-34856',
    year: '2025',
    doiUrl: 'https://doi.org/10.1021/acsomega.5c03887',
  },
  {
    title: 'A framework for explainable deep learning for aiding clinical applications of quantitative phase imaging',
    authors: 'Arora, Saransh, Tandon, Arushi, <strong>Ray, Srijan</strong>, Rajaram, Narasimhan, and Barman, Ishan',
    journal: 'Quantitative Phase Imaging X, SPIE',
    volume: null,
    number: null,
    pages: null,
    year: '2024',
    doiUrl: 'https://doi.org/10.1117/12.3002172',
  }
];
</script>


