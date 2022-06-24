<template>
  <nav
    class="flex flex-row py-2 justify-evenly border-b-4 neon-box bg-gray-900 z-50"
  >
    <NeonLink
      text="Rob Hall"
      link="#info"
      resp="hidden md:block"
      icon="fas fa-home"
    />
    <NeonLink
      text="Projects"
      link="#projects"
      resp="hidden md:block"
      icon="fas fa-folder-open"
    />
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
