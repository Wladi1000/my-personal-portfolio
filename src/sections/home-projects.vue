<script setup>
const projects = [
  {
    img: "/projects/02.jpeg",
    title: "Launch countdown timer",
    description:
      "Countdown timer set in a rocket launch. Challenge assigned from the page frontendmentor.io",
    tools: ["JavaScript", "Vue.js"],
    deploitment: "https://launch-countdown-timer-ws.netlify.app",
    repo: "https://github.com/Wladi1000/Launch-countdown-timer",
  },
  {
    img: "/projects/13.jpeg",
    title: "Personal Portfolio",
    description: "Personal portfolio for the presentation of my projects",
    tools: ["JavaScript","Vue.js", "Sass"],
    deploitment: "https://wladimirsanvicente.netlify.app",
    repo: "https://github.com/Wladi1000/my-personal-portfolio",
  },
  {
    img: "/projects/11.jpeg",
    title: "Samurai Game",
    description:
      "Game made with Vanilla JavaScript, made as a practice of the mentioned language",
    tools: ["JavaScript"],
    deploitment: "https://wladi1000-fighting-game.netlify.app",
    repo: "https://github.com/Wladi1000/fighting-game",
  },
  {
    img: "https://user-images.githubusercontent.com/108229029/216751013-8b2ac380-e068-448d-80d4-21b5b59647ea.png",
    title: "Spotify Clone",
    description:
      "Spotify Clone followed by Youtube tutorial by: @johnweeksdev",
    tools: ["JavaScript", "Vue.js", "Tailwind"],
    deploitment: null,
    repo: "https://github.com/Wladi1000/spotify-clone",
  },
  {
    img: "/projects/14.jpeg",
    title: "UCAB-Cunaguaro",
    description:
      "System for the automation of professional practice forms for the UCAB Extension Guayana",
    tools: ["JavaScript", "Vue.js", "Sass"],
    deploitment: null,
    repo: "https://github.com/Lu27656348/UCAB-Cunaguaro",
  },
  {
    img: "/projects/15.jpeg",
    title: "Todo App React + TypeScript",
    description:
      "Simple Todo list with React+TypeScript",
    tools: ["React", "TypeScript"],
    deploitment: "https://todo-app-ts-wladimirsanvicente.netlify.app",
    repo: "https://github.com/Wladi1000/Todo-app-Ts",
  }
];
</script>
<template>
  <section id="projects" class="proyectos-recientes section-clara d-flex flex-column">
    <h2 class="section-titulo">Projects</h2>
    <h3 class="section-descripcion">These are some projects I have done</h3>
    <!-- Galeria de proyectos -->
    <div class="container text-center proyectos-contenedor">
      <div class="row">
        <div
          class="col-12 col-md-6 col-lg-4"
          v-for="p in projects"
          :key="p.title"
        >
          <div class="proyecto">
            <img :src="p.img" :alt="p.description" />
            <div class="overlay">
              <p>{{ p.title }}</p>
              <div class="iconos-contenedor">
                <a 
                  v-if="p.repo"
                  :href="p.repo" 
                  target="_blanck" 
                  rel="noopener noreferrer"
                  ><i class="bi bi-github"></i
                ></a>
                <a
                  v-if="p.deploitment"
                  :href="p.deploitment"
                  target="_blanck"
                  rel="noopener noreferrer"
                  ><i class="bi bi-laptop"></i
                ></a>
              </div>
            </div>
          </div>
          <!-- Tecnologias usadas no funciona -->
          <!-- <div class="badges-contenedor">
            <div class="badge" v-for="b in p.tools" :key="b">
              {{ b }}
            </div>
          </div> -->
        </div>
      </div>
    </div>
    <a
      href="https://github.com/Wladi1000"
      target="_blank"
      rel="noopener noreferrer"
    >
      <button class="btn btn-info">
        Show More Projects
        <i class="bi bi-arrow-right-circle-fill"></i>
      </button>
    </a>
  </section>
</template>