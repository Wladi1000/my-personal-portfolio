<script setup>
const projects = [
  {
    img: "./src/assets/img/projects/02.jpeg",
    title: "Launch countdown timer",
    description:
      "Countdown timer set in a rocket launch. Challenge assigned from the page frontendmentor.io",
    tools: ["Vue.js"],
    deploitment: "https://launch-countdown-timer-ws.netlify.app",
    repo: "https://github.com/Wladi1000/Launch-countdown-timer",
  },
  {
    img: "./src/assets/img/projects/13.jpeg",
    title: "Personal Portfolio",
    description: "Personal portfolio for the presentation of my projects",
    tools: ["Vue.js", "Sass"],
    deploitment: "https://wladimirsanvicente.netlify.app",
    repo: "https://github.com/Wladi1000/my-personal-portfolio",
  },
  {
    img: "./src/assets/img/projects/11.jpeg",
    title: "Samurai Game",
    description:
      "Game made with Vanilla JavaScript, made as a practice of the mentioned language",
    tools: ["JavaScript"],
    deploitment: "https://wladi1000-fighting-game.netlify.app",
    repo: "https://github.com/Wladi1000/fighting-game",
  },
];
</script>
<template>
  <section class="proyectos-recientes section-clara d-flex flex-column">
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
                <a :href="p.repo" target="_blanck" rel="noopener noreferrer"
                  ><i class="bi bi-github"></i
                ></a>
                <a
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