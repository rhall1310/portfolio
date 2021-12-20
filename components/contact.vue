<template>
  <div
    class="bg-gray-800 p-2 w-full text-center rounded-lg justify-center items-center flex flex-col"
  >
    <h2 class="neon text-neon-light text-lg font-bold pb-2">Contact</h2>
    <form action="" class="flex flex-col align-middle gap-4">
      <div>
        <textarea
          name="msg"
          id="msg"
          cols="30"
          rows="10"
          placeholder="Your message"
          class="border-2 neon-box bg-transparent rounded-lg focus:border-neon-light text-white"
        ></textarea>
      </div>
      <div
        class="flex flex-col gap-6 pl-4 rounded-lg justify-center items-center"
      >
        <input
          type="email"
          name="email"
          id="email"
          placeholder="Your email"
          class="border-2 neon-box bg-transparent rounded-lg focus:border-neon-light text-white"
        />
        <input
          type="text"
          name="name"
          id="name"
          placeholder="Your name"
          class="border-2 neon-box bg-transparent rounded-lg focus:border-neon-light text-white"
        />
        <button type="submit" class="neon-glow-box border-2 rounded-lg w-24">
          Send
        </button>
      </div>
    </form>
  </div>
</template>

<script>
export default {}
</script>
