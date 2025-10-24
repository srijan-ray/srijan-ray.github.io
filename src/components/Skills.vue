<template>
  <section id="skills" class="py-20 bg-white">
    <div class="container mx-auto px-6 text-center">
      <h2 class="text-4xl font-bold text-center mb-16 text-slate-900">
        Technical Skills
      </h2>

      <div class="max-w-4xl mx-auto grid grid-cols-1 md:grid-cols-2 gap-x-12 gap-y-10 text-left">
        <!-- Dynamically create each skill category -->
        <div v-for="category in skillCategories" :key="category.title">
          <h3 class="text-xl font-bold text-slate-800 mb-4">{{ category.title }}</h3>
          <div class="flex flex-wrap gap-3">
            <span v-for="skill in category.skills" :key="skill" class="bg-slate-100 text-slate-700 font-semibold px-4 py-2 rounded-md shadow-sm">
              {{ skill }}
            </span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const skillCategories = [
  {
    title: 'Programming Languages',
    skills: ['Python', 'Java', 'JavaScript', 'TypeScript', 'HTML/CSS', 'Kotlin', 'C/C++']
  },
  {
    title: 'Machine Learning Frameworks',
    skills: ['TensorFlow', 'Keras', 'PyTorch']
  },
  {
    title: 'Frontend & Web',
    skills: ['Vue.js', 'Astro.js', 'React', 'Svelte.js', 'Tailwind CSS', 'Node.js']
  },
  {
    title: 'Backend & Databases',
    skills: ['FastAPI', 'Django', 'PostgreSQL', 'PostGIS', 'Redis']
  },
  {
    title: 'Libraries & Tools',
    skills: ['NumPy', 'Pandas', 'Matplotlib', 'Sci-Kit Learn', 'OpenCV', 'SQLAlchemy']
  },
  {
    title: 'Development Tools & Environments',
    skills: ['Vim', 'Docker', 'Git', 'Github', 'Linux', 'AWS']
  }
];
</script>
