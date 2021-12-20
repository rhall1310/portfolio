<template>
  <div class="bg-gray-900">
    <Header class="fixed top-0 w-screen h-12" />
    <div class="relative">
      <div id="info" class="flex flex-col pt-12 md:flex-row">
        <div
          id="sidebar-about"
          class="md:w-1/4 md:order-2 p-2 bg-gray-800 my-2"
        >
          <img
            src="~/assets/images/IMG_20210727_155113873.jpg"
            alt=""
            class="rounded-xl max-h-20 float-left pr-1"
          />
          <p class="text-white text-justify">
            I'm a front end web dev and designer who is passionate about Lorem
            ipsum dolor sit amet consectetur adipisicing elit. Soluta rerum
            corporis neque dolor iusto recusandae cum assumenda maxime facilis
            qui!
          </p>
        </div>

        <div id="main-about" class="p-2 md:w-3/4">
          <img src="" alt="" />
          <p class="text-white">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Suscipit
            ducimus debitis quisquam excepturi dolorem soluta, iure sit
            recusandae vero eaque voluptatibus ipsum dolorum itaque consequatur
            beatae asperiores? Provident, officiis voluptates! Aperiam laborum
            unde architecto minus modi? Eos distinctio non harum ex dolorem
            aspernatur minus, tempore nobis sunt odit illo dolores.
          </p>
        </div>
      </div>
      <h2
        class="neon text-neon-light underline text-center font-bold text-2xl pb-2"
        id="projects"
      >
        Projects
      </h2>
      <div class="flex flex-wrap flex-row">
        <Project
          v-for="project in projects"
          :key="project.index"
          :title="project.title"
          :text="project.text"
          :img="project.img"
          :code="project.code"
          :link="project.link"
          :icons="project.icons"
        />
      </div>

      <Contact id="contact" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          title: 'Svelte Weather',
          text: 'A simple weather app built with svelte',
          img: 'svelte_weather.png',
          code: 'https://github.com/rhall1310/svelte-weather',
          link: 'https://svelte-weather-rh1310-dev.netlify.app/',
          icons: ['fab fa-html5', 'fab fa-js'],
        },
        {
          title: 'Pothole Reporter',
          text: 'A pothole/highway issue reporting app made with Nuxt and styled with bootstrap',
          img: 'pothole_reporter.png',
          code: 'https://github.com/rhall1310/pothole-reporter',
          link: 'https://pothole-reporter-rh1310-dev.netlify.app/',
          icons: ['fab fa-html5', 'fab fa-js'],
        },
        {
          title: 'Pure CSS',
          text: 'A website built with pure CSS and HTML to demonstrate how much is possible without touching javascript at all',
          img: 'pothole_reporter.png',
          code: 'https://github.com/rhall1310/pothole-reporter',
          link: 'https://pothole-reporter-rh1310-dev.netlify.app/',
          icons: ['fab fa-html5', 'fab fa-css3'],
        },
      ],
    }
  },
}
</script>
