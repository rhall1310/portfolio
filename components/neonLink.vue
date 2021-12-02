<template>
  <a class="cursor-pointer neon-glow text-neon-light font-bold text-xl">
    {{ text }}
  </a>
</template>

<script>
export default {
  props: {
    text: String,
  },
}
</script>
