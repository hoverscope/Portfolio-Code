<template>
  <section id="my-work" class="text-white relative pt-0">
    <!-- My Work content container -->
    <div class="max-w-6xl mx-auto text-right px-4 sm:px-6 md:px-8">
      <!-- Updated Heading Style -->
      <h2
        class="text-3xl font-extrabold sm:text-4xl md:text-5xl lg:text-6xl xl:text-6xl mb-6 text-center"
      >
        My Work
      </h2>

      <!-- Grid Layout (2x2) with responsive grid columns -->
      <div
        class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2 lg:grid-cols-2 xl:grid-cols-2 gap-8"
      >
        <div
          v-for="(repo, index) in repositories"
          :key="index"
          class="bg-gray-800 rounded-lg p-6 shadow-lg hover:shadow-2xl transition duration-300"
        >
          <!-- Removed image here -->
          <h3 class="text-xl font-bold mb-4">{{ repo.name }}</h3>
          <p class="text-sm text-gray-400 mb-4">{{ repo.description }}</p>
          <a
            :href="repo.link"
            target="_blank"
            class="text-blue-400 hover:underline"
            >View Repo</a
          >
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "MyWork",
  data() {
    return {
      repositories: [
        {
          name: "📈 2DAttractorVisualizor",
          description:
            "A small-scale project built to visualize and animate Chaos Attractors using Vanilla JS. This is a practice project with a few built-in controls.",
          link: "https://github.com/hoverscope/2DAttractorVisualizor",
        },
        {
          name: "🧠 Custom Multi-Layer Perceptron on MNIST Dataset",
          description:
            "This project is a custom implementation of a Multi-Layer Perceptron (MLP) in Python, achieving a high accuracy of 98% on the MNIST dataset. 📈",
          link: "https://github.com/hoverscope/MNIST_MLP",
        },
        {
          name: "🕋 Prayer Time Chrome Extension",
          description:
            "This Chrome extension provides prayer times based on the user's city and location, helping you keep track of prayer timings directly in your browser. 🌙",
          link: "https://github.com/hoverscope/Prayer-time-chrome-extension",
        },
        {
          name: "🧛 vampDashSource",
          description: "Source Code for Game Built for Uni project",
          link: "https://github.com/hoverscope/vampDashSource",
        },
      ],
    };
  },
};
</script>

<style scoped>
/* Remove any default margins that might be causing the gap */
section {
  margin: 0;
}

/* Set the #my-work section for flex and right alignment */
#my-work {
  width: 100%;
  margin-top: 9rem; /* Added top margin for spacing */
  margin-bottom: 3rem; /* Added top margin for spacing */
}

/* Ensure the content inside #my-work is aligned to the right */
#my-work .max-w-6xl {
  text-align: center; /* Align content to the right */
}

/* Ensure responsiveness and make grid items aligned in rows */
@media (min-width: 640px) {
  #my-work .grid-cols-1 {
    grid-template-columns: repeat(
      2,
      1fr
    ); /* 2 columns for medium screens and larger */
  }
  #my-work .sm\:grid-cols-2 {
    grid-template-columns: repeat(2, 1fr); /* Grid template for 2 columns */
  }

  #my-work .text-left {
    text-align: left; /* Align text to the left on medium screens */
  }
}

@media (min-width: 768px) {
  #my-work .grid-cols-1 {
    grid-template-columns: repeat(2, 1fr); /* 2 columns for larger screens */
  }
}

@media (min-width: 1024px) {
  #my-work .grid-cols-1 {
    grid-template-columns: repeat(2, 1fr); /* 2 columns for large screens */
  }
}

@media (min-width: 1280px) {
  #my-work .grid-cols-1 {
    grid-template-columns: repeat(
      2,
      1fr
    ); /* Ensure 2 columns even on extra large screens */
  }
}
</style>
