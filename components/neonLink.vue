<template>
  <div class="cursor-pointer text-neon-light font-bold text-xl neon-glow">
    <a class="flex flex-row gap-2" :href="link" :target="target">
      <p :class="resp">{{ text }}</p>
      <Icons :icon="icon" />
    </a>
  </div>
</template>

<script>
export default {
  props: {
    text: String,
    link: String,
    icon: String,
    resp: String,
    target: String,
  },
}
</script>
