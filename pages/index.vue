<template>
  <div class="bg-gray-900">
    <Header class="fixed top-0 w-screen h-12" />

    <main
      id="info"
      class="flex flex-col pt-24 md:flex-row md:px-1 max-w-screen-xl mx-auto"
    >
      <div
        id="sidebar-about"
        class="md:w-1/3 lg:1/4 md:order-2 p-2 bg-gray-800 md:my-4 md:rounded-xl text-justify"
      >
        <h1 class="text-neon-light neon text-5xl text-center py-2 font-bold">
          Rob Hall
        </h1>

        <p class="text-neon-light neon text-xl py-2">
          I'm a web developer, designer and data specialist from the UK. I enjoy
          building intuitive and attractive UIs and layouts and helping people
          get the most out of their data and systems.
        </p>

        <p class="text-white px-1">
          I've been coding since I was in school and my goal is to make the
          internet more functional and better looking. I am also passionate
          about web accessibility and ensuring that as many people as possible
          can enjoy your website.
        </p>
        <p class="text-white px-1 py-3">
          I'm an organised and professional worker who is used to managing my
          own projects and delivering to deadlines
        </p>
      </div>

      <div id="main-about" class="p-2 md:w-2/3 lg:3/4 md:mr-6">
        <h2 class="neon text-neon-light underline font-bold text-3xl py-2">
          Skills
        </h2>
        <p class="text-white py-2">
          I am well versed in the core front end languages of HTML, CSS and
          Javascript. I have also worked extensively with other technologies
          such as Vue, Svelte, Django and various CSS frameworks including
          Bootstrap and Tailwind.
        </p>

        <div class="neon-box border-2 my-2"></div>
        <div class="flex gap-4 py-2 text-center flex-wrap justify-between px-3">
          <Icons
            v-for="skill in skillset"
            :key="skill"
            :icon="skill"
            class="neon text-neon-light text-5xl hover:text-pink-50"
          />
        </div>
        <div class="neon-box border-2 my-2"></div>

        <p class="text-white pt-4 text-justify">
          I also have extensive experience with creating Wordpress websites and
          custom themes. This includes using the ecommerce plugin WooCommerce to
          create successful storefronts. I'm always looking to learn more and
          further develop my skills.
        </p>
      </div>
    </main>
    <section class="max-w-screen-2xl mx-auto">
      <div id="projects" class="py-8"></div>
      <h2 class="neon text-neon-light underline text-center font-bold text-3xl">
        Projects
      </h2>
      <div
        class="flex flex-wrap flex-row mb-5 justify-between max-w-screen-xl mx-auto"
      >
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
    </section>
    <section id="contact" class="m-w-screen-2xl mx-auto my-16">
      <Contact />
    </section>

    <Footer />
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
          text: 'A pothole/highway issue reporting app. The frontend was made with Nuxt and styled with bootstrap. Django REST framework and Axios were used to build a REST API with a MYSQL database hosted on pythonanywhere to store submissions.',
          img: 'pothole_reporter.png',
          code: 'https://github.com/rhall1310/issue-reporter-frontend',
          link: 'https://report-rh1310-dev.netlify.app/',
          icons: [
            'fab fa-html5',
            'fab fa-js',
            'fab fa-vuejs',
            'fab fa-bootstrap',
          ],
        },
        {
          title: 'Sketch',
          text: 'A streamlined sketch/drawing app made with the HTML5 canvas element and vanilla Javascript',
          img: 'drawing.png',
          code: 'https://github.com/rhall1310/Drawing/',
          link: 'https://rhall1310.github.io/Drawing/',
          icons: ['fab fa-html5', 'fab fa-css3', 'fab fa-js'],
        },
      ],
      skillset: [
        'fab fa-html5',
        'fab fa-js',
        'fab fa-css3',
        'fab fa-vuejs',
        'fab fa-bootstrap',
        'fab fa-wordpress',
        'fab fa-python',
      ],
    }
  },
}
</script>
