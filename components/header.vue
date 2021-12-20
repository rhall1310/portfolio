<template>
  <nav
    class="flex flex-row py-2 justify-evenly border-b-4 neon-box bg-gray-900 z-50"
  >
    <NeonLink text="Info" link="#info" />
    <NeonLink text="Projects" link="#projects" />
    <NeonLink
      text="Github"
      link="https://github.com/rhall1310"
      resp="hidden md:block"
      icon="fab fa-github"
      target="blank"
    />
    <NeonLink
      text="Contact"
      resp="hidden md:block"
      icon="fas fa-envelope"
      link="#contact"
    />
  </nav>
</template>

<script>
export default {}
</script>

<style></style>
