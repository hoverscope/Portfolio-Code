<template>
  <section id="about" class="text-white py-6 relative min-h-[60vh]">
    <div class="relative z-10 pb-8 max-w-6xl mx-auto px-4 sm:px-6 md:px-8">
      <!-- Removed text-center from section, and heading is aligned to the left -->
      <h2
        class="text-3xl font-extrabold sm:text-4xl md:text-5xl lg:text-6xl xl:text-6xl mb-6 text-left"
      >
        About Me
      </h2>

      <p
        class="text-sm mt-4 text-base sm:text-lg md:text-xl lg:text-2xl text-gray-200 text-left"
      >
        I am a passionate developer with a strong interest in Data Science. I
        love creating innovative solutions and modern web applications, while
        also exploring the world of data analysis and machine learning.
      </p>

      <p
        class="text-sm mt-4 text-base sm:text-lg md:text-xl lg:text-2xl text-gray-200 text-left"
      >
        I have experience with both frontend and backend technologies, such as
        Node.js and Vue.js, as well as leveraging data science techniques to
        derive meaningful insights.
      </p>

      <p
        class="text-sm mt-4 text-base sm:text-lg md:text-xl lg:text-2xl text-gray-200 text-left"
      >
        I have maintained First Honour results throughout my studies so far.
        Currently, I live in Dubai and am pursuing my B.Sc. Honours in
        Information Technology at Middlesex University Dubai.
      </p>

      <h3
        class="text-lg font-semibold sm:text-xl md:text-2xl lg:text-3xl xl:text-3xl mt-12 mb-6 text-left"
      >
        Skills
      </h3>

      <div class="flex flex-wrap gap-4 mt-8">
        <span class="bg-gray-300 text-black py-1 px-4 rounded-full text-lg"
          >Node.js</span
        >
        <span class="bg-gray-300 text-black py-1 px-4 rounded-full text-lg"
          >Vue.js</span
        >
        <span class="bg-gray-300 text-black py-1 px-4 rounded-full text-lg"
          >Data Science</span
        >
        <span class="bg-gray-300 text-black py-1 px-4 rounded-full text-lg"
          >Machine Learning</span
        >
        <span class="bg-gray-300 text-black py-1 px-4 rounded-full text-lg"
          >Python</span
        >
        <span class="bg-gray-300 text-black py-1 px-4 rounded-full text-lg"
          >MongoDB</span
        >
        <span class="bg-gray-300 text-black py-1 px-4 rounded-full text-lg"
          >Java</span
        >
        <span class="bg-gray-300 text-black py-1 px-4 rounded-full text-lg"
          >Python</span
        >
        <span class="bg-gray-300 text-black py-1 px-4 rounded-full text-lg"
          >C#</span
        >
        <span class="bg-gray-300 text-black py-1 px-4 rounded-full text-lg"
          >Javascript</span
        >
        <span class="bg-gray-300 text-black py-1 px-4 rounded-full text-lg"
          >Frontend Development</span
        >
        <span class="bg-gray-300 text-black py-1 px-4 rounded-full text-lg"
          >Backend Development</span
        >
        <span class="bg-gray-400 text-black py-1 px-4 rounded-full text-lg"
          >SQL Server</span
        >
        <span class="bg-gray-400 text-black py-1 px-4 rounded-full text-lg"
          >Management</span
        >
        <span class="bg-gray-400 text-black py-1 px-4 rounded-full text-lg"
          >Data Analytics</span
        >
        <span class="bg-gray-400 text-black py-1 px-4 rounded-full text-lg"
          >Machine Learning</span
        >
        <span class="bg-gray-400 text-black py-1 px-4 rounded-full text-lg"
          >2D/3D Design</span
        >
        <span class="bg-gray-400 text-black py-1 px-4 rounded-full text-lg"
          >Visualization</span
        >
      </div>

      <h3
        class="text-lg font-semibold sm:text-xl md:text-2xl lg:text-3xl xl:text-3xl mt-12 mb-6 text-left"
      >
        Languages
      </h3>

      <div class="flex flex-wrap gap-4 mt-10">
        <div class="bg-gray-300 text-black py-1 px-4 rounded-full text-lg">
          English - Fluent
        </div>

        <div class="bg-gray-300 text-black py-1 px-4 rounded-full text-lg">
          Urdu - Native
        </div>
        <div class="bg-gray-300 text-black py-1 px-4 rounded-full text-lg">
          Hindi - Fluent
        </div>
      </div>
    </div>

    <div class="mt-12">
      <button
        @click="scrollToAbout"
        class="explore-button flex items-center justify-center space-x-2 bg-gray-800 px-6 py-4 rounded-lg shadow-lg mx-auto hover:bg-gray-700 transition-colors sm:px-4 sm:py-3"
      >
        <span>Work Experience</span>
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
      const aboutSection = document.querySelector("#work");
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

/* Set the #about section for padding and alignment */
#about {
  width: 100%;
  padding-top: 6rem; /* Adjust top padding for spacing */
}

/* Ensure the content inside #about is aligned to the left */
#about .max-w-6xl {
  text-align: left; /* Align content to the left */
}

/* Responsive adjustments for text alignment and padding */
#about h2 {
  font-size: 2rem;
}

/* Ensure responsiveness */
@media (min-width: 640px) {
  #about h2 {
    font-size: 3rem;
  }

  #about p {
    font-size: 1.125rem; /* Medium size text */
  }

  #about h3 {
    font-size: 2.25rem; /* Skills section heading size */
  }
}

@media (min-width: 768px) {
  #about h2 {
    font-size: 4rem;
  }

  #about p {
    font-size: 1.25rem; /* Larger text on tablets */
  }
}

@media (min-width: 1024px) {
  #about h2 {
    font-size: 5rem;
  }

  #about p {
    font-size: 1.5rem; /* Larger text on larger screens */
  }

  #about h3 {
    font-size: 4rem; /* Skills section heading size */
  }
}

/* Styling for the skill tags */
#about .flex-wrap {
  display: flex;
  flex-wrap: wrap;
}

#about .bg-blue-600 {
  background-color: #3b82f6;
}

#about .bg-green-600 {
  background-color: #10b981;
}

#about .bg-red-600 {
  background-color: #ef4444;
}

#about .bg-yellow-600 {
  background-color: #f59e0b;
}

#about .bg-purple-600 {
  background-color: #8b5cf6;
}

#about .bg-indigo-600 {
  background-color: #6366f1;
}
</style>
