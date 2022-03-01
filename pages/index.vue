<template>
  <div class="bg-gray-900">
    <Header class="fixed top-0 w-screen h-12" />

    <main
      id="info"
      class="flex flex-col pt-12 md:flex-row md:px-1 max-w-screen-2xl mx-auto"
    >
      <div
        id="sidebar-about"
        class="md:w-1/3 lg:1/4 md:order-2 p-2 bg-gray-800 md:my-4 md:rounded-xl"
      >
        <h1 class="text-neon-light neon text-4xl text-center py-2">Rob Hall</h1>

        <img
          src="~/assets/images/IMG_20210727_155113873.jpg"
          alt=""
          class="rounded-3xl max-h-28 float-left border-2 border-neon-light mr-2"
        />
        <p class="text-neon-light neon text-xl py-2">
          I'm a front end web dev and designer from the UK. I enjoy building
          intuitive and attractive UIs and layouts.
        </p>

        <p class="text-white px-1">
          I've been coding since I was in school and My goal is to make the
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
        <h2 class="neon text-neon-light underline font-bold text-2xl py-2">
          Skillset
        </h2>
        <p class="text-white py-2">
          I am well versed in the core front end languages of HTML, CSS and
          Javascript. I have also worked extensively with other technologies
          such as Vue, Svelte and various CSS frameworks including Bootstrap and
          Tailwind.
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
    <section id="projects" class="max-w-screen-2xl mx-auto">
      <h2
        class="neon text-neon-light underline text-center font-bold text-2xl py-8"
      >
        Projects
      </h2>
      <div class="flex flex-wrap flex-row mb-5 justify-between">
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
    <section id="contact" class="m-w-screen-2xl mx-auto">
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
          text: 'A pothole/highway issue reporting app made with Nuxt and styled with bootstrap',
          img: 'pothole_reporter.png',
          code: 'https://github.com/rhall1310/pothole-reporter',
          link: 'https://pothole-reporter-rh1310-dev.netlify.app/',
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
        {
          title: 'CSS Only',
          text: 'A simple static site built with CSS and HTML only to demonstrate responsive design principles',
          img: 'css_only.png',
          code: 'https://github.com/rhall1310/CSS-Only',
          link: 'https://rhall1310.github.io/CSS-Only/',
          icons: ['fab fa-html5', 'fab fa-css3'],
        },
        {
          title: 'An-UK',
          text: 'A site built for a small online business using Wordpress and WooCommerce',
          img: 'an_uk.png',
          code: 'https://github.com/rhall1310',
          link: 'https://an-uk.com/',
          icons: ['fab fa-wordpress', 'fab fa-php', 'fab fa-css3'],
        },
      ],
      skillset: [
        'fab fa-html5',
        'fab fa-js',
        'fab fa-css3',
        'fab fa-vuejs',
        'fab fa-bootstrap',
        'fab fa-wordpress',
      ],
    }
  },
}
</script>
