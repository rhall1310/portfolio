<template>
  <div>
    <button @click="show = true">Open</button>

    <div
      class="modal bg-gray-600 w-full h-full fixed top-0 right-0 left-0 z-50"
      v-show="show"
    >
      Boo
      <button @click="show = false">Close</button>
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
}
</script>

<style></style>
