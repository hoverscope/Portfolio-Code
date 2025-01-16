<template>
  <section id="contact" class="text-white py-16">
    <div class="max-w-6xl mx-auto text-center px-4 sm:px-6 md:px-8">
      <h2 class="text-3xl font-extrabold sm:text-4xl mb-6">Contact Me</h2>
      <p class="text-gray-400 mb-6">
        Feel free to reach out! I'd love to hear from you.
      </p>
      <!-- Button for opening email client -->
      <button
        @click="sendEmail"
        class="inline-block px-8 py-3 bg-blue-500 hover:bg-blue-700 text-white font-bold rounded-lg transition duration-300 z-10"
      >
        Send Email
      </button>
    </div>
  </section>
</template>

<script>
export default {
  name: "Contact",
  methods: {
    sendEmail() {
      window.location.href =
        "mailto:sohail50043@gmail.com?subject=Contact%20from%20Portfolio&body=Hello,%20I%20would%20like%20to%20get%20in%20touch...";
    },
  },
};
</script>

<style scoped>
button {
  display: inline-block;
  z-index: 10; /* Ensure the button is clickable and on top */
}

button:hover {
  background-color: #4b6cb7;
}
</style>
