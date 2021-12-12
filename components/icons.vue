<template>
  <div>
    <i :class="icon"></i>
  </div>
</template>

<script>
export default {
  props: {
    icon: String,
  },
}
</script>

<style scoped>
@import 'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css';
</style>
