<template>
  <header class="text-white p-4">
    <div class="flex justify-between items-center max-w-screen-xl mx-auto">
      <!-- Navigation Links -->
      <nav class="space-x-6 hidden md:flex">
        <a href="#about" class="text-white hover:text-blue-400 transition"
          >About</a
        >
        <a href="#contact" class="text-white hover:text-blue-400 transition"
          >Contact</a
        >
      </nav>

      <!-- Mobile Menu (Hamburger) -->
      <button @click="toggleMobileMenu" class="md:hidden text-white">
        <span class="material-icons">menu</span>
      </button>
    </div>

    <!-- Mobile Menu -->
    <div v-if="isMobileMenuOpen" class="md:hidden">
      <nav class="flex flex-col items-center space-y-4 py-4 bg-gray-800">
        <a href="#home" class="text-white hover:text-blue-400 transition"
          >Home</a
        >
        <a href="#services" class="text-white hover:text-blue-400 transition"
          >Services</a
        >
        <a href="#about" class="text-white hover:text-blue-400 transition"
          >About</a
        >
        <a href="#contact" class="text-white hover:text-blue-400 transition"
          >Contact</a
        >
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      isMobileMenuOpen: false,
    };
  },
  methods: {
    toggleMobileMenu() {
      this.isMobileMenuOpen = !this.isMobileMenuOpen;
    },
    scrollToSection(event, sectionId) {
      event.preventDefault();
      const section = document.querySelector(sectionId);
      if (section) {
        section.scrollIntoView({
          behavior: "smooth",
          block: "start",
        });
      }
    },
  },
};
</script>

<style scoped>
/* Modern design styles */
header {
  background-color: #1a202c; /* Dark background */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Subtle shadow */
}

nav a {
  font-weight: 600;
  font-size: 1rem;
}

nav a:hover {
  color: #63b3ed; /* Light blue color on hover */
}

.material-icons {
  font-size: 2rem;
}

@media (max-width: 768px) {
  nav a {
    font-size: 1.25rem;
  }
}
</style>
