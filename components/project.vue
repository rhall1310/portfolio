<template>
  <div class="text-white md:w-1/3 mt-2">
    <div
      class="border-neon-dark border-2 p-1 rounded-lg bg-gray-800 m-2 hover:border-neon-light group h-full flex flex-col"
    >
      <a target="blank" :href="link">
        <div class="grid grid-cols-4 grid-rows-5 mx-2 pb-1">
          <h2
            class="neon text-neon-light text-lg font-bold row-start-1 h-8 col-start-1 col-span-5 z-10 bg-gray-900 bg-opacity-90 text-center group-hover:underline"
          >
            {{ title }}
          </h2>
          <img
            :src="require(`~/assets/images/${this.img}`)"
            class="row-start-1 row-span-5 col-start-1 col-span-5 w-full project-img"
          />
        </div>
      </a>
      <p class="neon text-neon-light flex-grow">
        {{ text }}
      </p>

      <div
        class="flex flex-row gap-4 font-semibold underline py-2 justify-center"
      >
        <a target="blank" :href="code">Source Code</a
        ><a target="blank" :href="link">Live Demo</a>
      </div>
      <div
        class="neon text-neon-light flex flex-row gap-4 text-4xl justify-center"
      >
        <Icons
          v-for="icon in icons"
          :icon="icon"
          :key="icon.index"
          class="hover:text-pink-50"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      show: false,
    }
  },
  props: {
    title: String,
    text: String,
    img: String,
    code: String,
    link: String,
    icons: Array,
  },
}
</script>

<style></style>
