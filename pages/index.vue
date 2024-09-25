<template>
    <div class="min-h-screen bg-gray-900 text-white font-sans">
      <!-- Navbar -->
      <nav class="p-5 bg-gray-800 shadow-lg">
        <div class="container mx-auto flex justify-between items-center">
          <h1 class="text-2xl font-bold">Hai, Welcome at Angger Abed Nego Portofolio</h1>
          <ul class="flex space-x-4">
            <li><a href="#about" class="hover:text-teal-300">About</a></li>
            <li><a href="#projects" class="hover:text-teal-300">Projects</a></li>
            <li><a href="#contact" class="hover:text-teal-300">Contact</a></li>
          </ul>
        </div>
      </nav>
  
      <!-- Hero Section -->
      <section class="flex items-center justify-center min-h-screen bg-cover bg-center" :style="{ backgroundImage: 'url(hero-bg.jpg)' }">
        <div class="text-center">
          <h2 class="text-4xl md:text-6xl font-bold mb-4 animate-float">Hi, I'm Angger</h2>
          <p class="text-xl md:text-2xl">A Passionate IT Student & Developer</p>
        </div>
      </section>
  
      <!-- About Section -->
      <section id="about" class="py-16 bg-gray-800">
        <div class="container mx-auto px-4">
          <h3 class="text-3xl font-semibold mb-6">About Me</h3>
          <p>Nama saya Angger Abednego, Saya adalah mahasiswa jurusan Teknologi Informasi di Universitas Brawijaya. Saya memiliki minat besar di bidang teknologi, branding, dan digital marketing.</p>
        </div>
      </section>
  
      <!-- Projects Section -->
      <section id="projects" class="py-16 bg-gray-900">
        <div class="container mx-auto px-4">
          <h3 class="text-3xl font-semibold mb-6">Projects</h3>
          <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div
              v-for="project in projects"
              :key="project.title"
              class="bg-gray-800 p-6 rounded-lg hover:scale-105 transition-transform duration-300"
              @mouseover="hoverEffect($event)"
              @mouseleave="resetEffect($event)"
            >
              <h4 class="text-xl font-semibold">{{ project.title }}</h4>
              <p>{{ project.description }}</p>
            </div>
          </div>
        </div>
      </section>
  
      <!-- Contact Section -->
      <section id="contact" class="py-16 bg-gray-800">
        <div class="container mx-auto px-4 text-center">
          <h3 class="text-3xl font-semibold mb-6">Contact</h3>
          <div class="flex justify-center space-x-4">
            <a href="https://www.linkedin.com/in/angger-abednego-1404-bdvy" class="hover:scale-110 transition-transform"><img src="/linkedin.png" alt="LinkedIn" class="w-8 h-8"></a>
            <a href="mailto:anggerabednego14@gmail.com" class="hover:scale-110 transition-transform"><img src="/email.png" alt="Email" class="w-8 h-8"></a>
          </div>
        </div>
      </section>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        projects: [
          { title: 'Sistem Lelang', description: 'Aplikasi sistem lelang berbasis web menggunakan Java, HTML, dan PHP.' },
          { title: 'Sistem Akademik', description: 'Basis data sistem akademik untuk perguruan tinggi.' },
          { title: 'E-commerce Sepatu', description: 'Aplikasi e-commerce untuk sepatu lokal Indonesia.' }
        ]
      };
    },
    methods: {
      hoverEffect(event) {
        event.target.classList.add('hovered');
      },
      resetEffect(event) {
        event.target.classList.remove('hovered');
      }
    }
  };
  </script>
  
  <style scoped>
  .hovered {
    transform: scale(1.1);
    transition: all 0.3s ease-in-out;
  }
  </style>
  