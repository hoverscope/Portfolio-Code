<template>
  <section id="education" class="text-white relative pt-0">
    <!-- Education content container -->
    <div class="max-w-6xl mx-auto text-right px-4 sm:px-6 md:px-8">
      <h2
        class="text-3xl font-extrabold sm:text-4xl md:text-5xl lg:text-6xl xl:text-6xl mb-6 text-left"
      >
        Education
      </h2>

      <!-- Education Entry -->
      <div
        class="flex items-center justify-between bg-gray-800 p-6 rounded-lg mb-6 flex-col sm:flex-row"
      >
        <!-- Circle on the left -->
        <div
          class="w-16 h-16 bg-blue-500 rounded-full flex items-center justify-center text-white font-bold text-lg mb-4 sm:mb-0"
        >
          <span>1</span>
          <!-- Can replace this with an icon or number -->
        </div>

        <!-- Degree and Institution below the circle (stacked on small screens, inline on larger ones) -->
        <div class="flex-1 ml-4 flex flex-col items-start sm:items-start">
          <h3 class="text-xl font-semibold">
            B.Sc. Honours in Information Technology
          </h3>
          <p class="text-sm text-gray-400">
            Middlesex University Dubai, United Arab Emirates
          </p>
        </div>

        <!-- Time (When to When) on the right -->
        <div class="flex-shrink-0 mt-4 sm:mt-0">
          <span class="text-gray-400">September 2020 -</span>
        </div>
      </div>

      <!-- Another Education Entry -->
      <div
        class="flex items-center justify-between bg-gray-800 p-6 rounded-lg mb-6 flex-col sm:flex-row"
      >
        <!-- Circle on the left -->
        <div
          class="w-16 h-16 bg-green-500 rounded-full flex items-center justify-center text-white font-bold text-lg mb-4 sm:mb-0"
        >
          <span>2</span>
          <!-- Replace with appropriate content -->
        </div>

        <!-- Degree and Institution below the circle (stacked on small screens, inline on larger ones) -->
        <div class="flex-1 ml-4 flex flex-col items-start sm:items-start">
          <h3 class="text-xl font-semibold">Higher Secondary Education</h3>
          <p class="text-sm text-gray-400">
            The Indian High School Dubai, United Arab Emirates
          </p>
        </div>

        <!-- Time (When to When) on the right -->
        <div class="flex-shrink-0 mt-4 sm:mt-0">
          <span class="text-gray-400">2020 - 2022</span>
        </div>
      </div>
    </div>

    <div class="mt-12">
      <button
        @click="scrollToAbout"
        class="explore-button flex items-center justify-center space-x-2 bg-gray-800 px-6 py-4 rounded-lg shadow-lg mx-auto hover:bg-gray-700 transition-colors sm:px-4 sm:py-3"
      >
        <span>View My Work</span>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          class="w-5 h-5 animate-float"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M19 14l-7 7m0 0l-7-7m7 7V3"
          />
        </svg>
      </button>
    </div>
  </section>
</template>

<script>
export default {
  methods: {
    scrollToAbout() {
      // Find the about section
      const aboutSection = document.querySelector("#my-work");
      if (aboutSection) {
        // Calculate the position to scroll to (subtract an offset for better alignment)
        const offset = 50; // Adjust this value to fit the desired gap
        const position = aboutSection.offsetTop - offset;

        // Scroll to the section with smooth behavior
        window.scrollTo({
          top: position,
          behavior: "smooth",
        });
      }
    },
  },
};
</script>

<style scoped>
/* Remove any default margins that might be causing the gap */
section {
  margin: 0;
}

/* Set the #education section for flex and right alignment */
#education {
  width: 100%;
  margin-top: 6rem; /* Added top margin for spacing */
}

/* Ensure the content inside #education is aligned to the right */
#education .max-w-6xl {
  text-align: right; /* Align content to the right */
}

/* Style for the education entry circle */
#education .w-16 {
  width: 4rem; /* Circle width */
  height: 4rem; /* Circle height */
}

/* Optional: Style for the circle to add icon/font */
#education .bg-blue-500 {
  background-color: #3b82f6;
}

/* Make sure degree and institution are aligned on the left below the circle */
#education .flex-col.items-start {
  text-align: left; /* Align text to the left */
}

/* Ensure responsiveness */
@media (min-width: 640px) {
  #education .flex-col.sm\:flex-row {
    flex-direction: row; /* Switch to row on larger screens */
  }

  #education .sm\:mt-0 {
    margin-top: 0; /* Remove top margin on larger screens */
  }

  #education .sm\:items-start {
    align-items: flex-start; /* Align items to the start on larger screens */
  }

  #education .sm\:mb-0 {
    margin-bottom: 0; /* Remove bottom margin on larger screens */
  }
}
</style>
