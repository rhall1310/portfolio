<template>
  <footer
    class="flex neon-box bg-neon-dark min-h-2 mt-8 text-white justify-between"
  >
    <p>
      <i class="fas fa-copyright p-2">opyright Rob Hall {{ currentYear }}</i>
    </p>
    <a href="#info" class="font-semibold self-center mr-4">Back to top</a>
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
