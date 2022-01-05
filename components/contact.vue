<template>
  <div
    class="bg-gray-800 m-2 shadow-2xl p-2 w-12/12 text-center rounded-lg justify-center items-center flex flex-col md:w-3/5 lg:w-3/6 md:m-auto"
  >
    <h2 class="neon text-neon-light text-2xl font-bold pb-2">Contact</h2>
    <form
      action=""
      class="flex flex-col align-middle gap-4 w-full md:flex-row md:gap-0"
      data-netlify="true"
      name="contact"
    >
      <textarea
        name="msg"
        id="msg"
        cols="30"
        rows="10"
        placeholder="Your message"
        class="border-2 neon-box bg-transparent rounded-lg focus:border-neon-light text-white w-10/12 m-auto md:mb-4 md:ml-4 p-1 placeholder-neon-light"
        required
      ></textarea>

      <div
        class="flex flex-col gap-6 pl-4 rounded-lg justify-center items-center"
      >
        <input
          type="email"
          name="email"
          id="email"
          placeholder="Your email"
          class="border-2 neon-box bg-transparent rounded-lg focus:border-neon-light text-white p-1 placeholder-neon-light"
          required
        />

        <input
          type="text"
          name="name"
          id="name"
          placeholder="Your name"
          class="border-2 neon-box bg-transparent rounded-lg focus:border-neon-light text-white p-1 placeholder-neon-light"
          required
        />
        <button
          type="submit"
          class="neon-glow-box border-2 rounded-lg w-24 mb-4"
        >
          Send
        </button>
      </div>
    </form>
  </div>
</template>

<script>
export default {}
</script>
