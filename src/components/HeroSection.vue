<template>
  <section
    id="hero"
    class="text-white min-h-screen flex items-center justify-center text-center relative px-4 sm:px-6 md:px-8"
  >
    <!-- Retro Grid for background effect -->
    <div
      class="retro-grid"
      :style="{
        '--cell-size': '60px',
        '--opacity': '0.2',
        '--light-line': 'gray',
        '--dark-line': 'gray',
      }"
    ></div>

    <!-- Content -->
    <div class="relative z-10">
      <!-- Main Heading -->
      <h1
        class="text-3xl font-extrabold sm:text-4xl md:text-5xl lg:text-6xl xl:text-6xl"
      >
        <span>Hi, I am</span>
        <br />
        <span
          class="text-4xl font-extrabold sm:text-5xl md:text-6xl lg:text-7xl xl:text-[6rem]"
        >
          Mohammed
          <span
            class="text-4xl font-extrabold sm:text-5xl md:text-6xl lg:text-7xl xl:text-[6rem] text-gray-300"
            >Sohail👋</span
          >
        </span>
      </h1>

      <!-- Subtext -->
      <p
        class="text-sm mt-4 mx-auto text-base sm:text-lg md:text-xl lg:text-2xl max-w-4xl text-gray-200"
      >
        Final Year Student |🎓 Pursuing B.Sc. Honours in Information Technology
        at Middlesex University Dubai
      </p>

      <!-- Dock for social links -->
      <div class="mt-8 flex justify-center space-x-6">
        <!-- LinkedIn -->
        <a
          href="https://www.linkedin.com/in/mohammed-sohail-184695239/"
          target="_blank"
          class="text-blue-400 hover:text-blue-600 transition"
          aria-label="LinkedIn"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="currentColor"
            viewBox="0 0 24 24"
            class="w-6 h-6"
          >
            <path
              d="M22.23 0H1.77A1.77 1.77 0 000 1.77v20.45A1.77 1.77 0 001.77 24h20.45A1.77 1.77 0 0024 22.23V1.77A1.77 1.77 0 0022.23 0zM7.12 20.45H3.56V9h3.56zM5.34 7.45a2.07 2.07 0 11.01-4.14 2.07 2.07 0 01-.01 4.14zm15.11 13h-3.56v-5.6c0-1.34-.02-3.07-1.87-3.07-1.88 0-2.17 1.46-2.17 2.97v5.7H9.3V9h3.42v1.56h.05a3.76 3.76 0 013.38-1.86c3.62 0 4.29 2.38 4.29 5.47z"
            />
          </svg>
        </a>

        <!-- GitHub -->
        <a
          href="https://github.com/hoverscope"
          target="_blank"
          class="text-gray-400 hover:text-gray-200 transition"
          aria-label="GitHub"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="currentColor"
            viewBox="0 0 24 24"
            class="w-6 h-6"
          >
            <path
              d="M12 .5A11.5 11.5 0 00.5 12c0 5.08 3.29 9.39 7.85 10.93.57.1.77-.24.77-.54 0-.27-.01-1-.01-1.95-3.2.69-3.87-1.55-3.87-1.55-.52-1.3-1.27-1.65-1.27-1.65-1.04-.72.08-.7.08-.7 1.16.08 1.77 1.19 1.77 1.19 1.03 1.75 2.7 1.25 3.36.96.1-.74.4-1.25.73-1.54-2.55-.29-5.23-1.28-5.23-5.7 0-1.26.45-2.29 1.19-3.1-.12-.3-.52-1.52.11-3.17 0 0 .98-.31 3.21 1.18.93-.26 1.93-.38 2.92-.38.99 0 1.99.12 2.92.38 2.22-1.49 3.21-1.18 3.21-1.18.63 1.65.24 2.87.12 3.17.74.81 1.19 1.84 1.19 3.1 0 4.43-2.69 5.41-5.24 5.7.41.36.77 1.08.77 2.18 0 1.58-.01 2.85-.01 3.23 0 .3.2.65.78.54A11.5 11.5 0 0023.5 12 11.5 11.5 0 0012 .5z"
            />
          </svg>
        </a>

        <!-- Email -->
        <a
          href="mailto:sohail50043@gmail.com"
          class="text-red-400 hover:text-red-600 transition"
          aria-label="Email"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 48 48"
            class="w-6 h-6"
          >
            <path
              fill="#4caf50"
              d="M45,16.2l-5,2.75l-5,4.75L35,40h7c1.657,0,3-1.343,3-3V16.2z"
            ></path>
            <path
              fill="#1e88e5"
              d="M3,16.2l3.614,1.71L13,23.7V40H6c-1.657,0-3-1.343-3-3V16.2z"
            ></path>
            <polygon
              fill="#e53935"
              points="35,11.2 24,19.45 13,11.2 12,17 13,23.7 24,31.95 35,23.7 36,17"
            ></polygon>
            <path
              fill="#c62828"
              d="M3,12.298V16.2l10,7.5V11.2L9.876,8.859C9.132,8.301,8.228,8,7.298,8h0C4.924,8,3,9.924,3,12.298z"
            ></path>
            <path
              fill="#fbc02d"
              d="M45,12.298V16.2l-10,7.5V11.2l3.124-2.341C38.868,8.301,39.772,8,40.702,8h0 C43.076,8,45,9.924,45,12.298z"
            ></path>
          </svg>
        </a>
      </div>

      <!-- Explore and Download CV Buttons -->
      <div
        class="mt-12 flex flex-col sm:flex-row justify-center space-y-4 sm:space-y-0 sm:space-x-4"
      >
        <!-- Explore Button -->
        <button
          @click="scrollToAbout"
          class="explore-button flex items-center justify-center space-x-2 bg-gray-800 px-6 py-4 rounded-lg shadow-lg hover:bg-gray-700 transition-colors sm:px-4 sm:py-3"
        >
          <span>Explore</span>
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

        <!-- Download CV Button -->
        <button
          @click="downloadCV"
          class="explore-button flex items-center justify-center space-x-2 bg-gray-800 px-6 py-4 rounded-lg shadow-lg hover:bg-gray-700 transition-colors sm:px-4 sm:py-3"
        >
          <span>Download CV</span>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            class="w-5 h-5"
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
    </div>
  </section>
</template>

<script>
export default {
  methods: {
    scrollToAbout() {
      const aboutSection = document.getElementById("about");
      aboutSection.scrollIntoView({ behavior: "smooth" });
    },
    downloadCV() {
      window.open("/path-to-your-cv.pdf", "_blank");
    },
  },
};
</script>

<style scoped>
.retro-grid {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: linear-gradient(
      var(--grid-angle),
      var(--light-line) 1px,
      transparent 1px
    ),
    linear-gradient(90deg, var(--dark-line) 1px, transparent 1px);
  background-size: var(--cell-size) var(--cell-size);
  background-position: center;
  opacity: var(--opacity);
  z-index: -1;
}
</style>
