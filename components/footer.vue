<template>
  <footer
    class="flex bg-gray-900 min-h-2 text-white justify-between py-5 md:mx-8"
  >
    <p>
      <i class="fas fa-copyright p-2 text-neon">
        <p class="inline text-white">opyright Rob Hall {{ currentYear }}</p></i
      >
    </p>
    <a href="#info" class="font-semibold self-center mr-4 underline">
      <p class="hidden md:block">Back to top</p>
      <Icons icon="fas fa-arrow-up underline" class="md:hidden" />
    </a>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      currentYear: new Date().getFullYear(), // 2020
    }
  },
}
</script>
