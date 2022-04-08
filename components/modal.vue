<template>
  <div>
    <button @click="show = true">Open</button>

    <div
      class="modal bg-gray-600 w-full h-full fixed top-0 right-0 left-0 z-50 flex bg-opacity-40"
      v-show="show"
    >
      <div class="inner-modal bg-black w-1/2 h-1/2 m-auto">
        <button @click="show = false" class="">Close</button>
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
}
</script>

<style></style>
