<template>
  <div>
    <!-- Hero Section with Rounded Rectangle and Retro Grid -->
    <div
      class="relative rounded-lg overflow-hidden shadow-lg mx-4 md:mx-16 my-8 border border-gray-200 border-opacity-20"
    >
      <div class="retro-grid"></div>

      <HeroSection />
      <AboutSection />

      <!-- Work Experience Section with Scroll Fade-in -->
      <FadeInOnScroll>
        <WorkExperience />
      </FadeInOnScroll>

      <!-- Education Section with Scroll Fade-in -->
      <FadeInOnScroll>
        <Education />
      </FadeInOnScroll>

      <FadeInOnScroll>
        <MyWork />
      </FadeInOnScroll>

      <FadeInOnScroll>
        <Contact />
      </FadeInOnScroll>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import HeroSection from "./components/HeroSection.vue";
import AboutSection from "./components/About.vue";
import WorkExperience from "./components/WorkExperience.vue";
import Education from "./components/Education.vue";
import FadeInOnScroll from "./components/FadeInOnScroll.vue";
import MyWork from "./components/MyWork.vue";
import Contact from "./components/Contact.vue";

export default {
  name: "App",
  components: {
    Header,
    HeroSection,
    AboutSection,
    WorkExperience,
    Education,
    FadeInOnScroll,
    MyWork,
    Contact,
  },
};
</script>

<style>
/* Base container styles */
.relative {
  position: relative;
}

/* Retro grid background styles */
.retro-grid {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-image: linear-gradient(
      to right,
      rgba(255, 255, 255, 0.05) 1px,
      transparent 1px
    ),
    linear-gradient(to bottom, rgba(255, 255, 255, 0.05) 1px, transparent 1px);
  background-size: 60px 60px;
  background-repeat: repeat;
  opacity: 0.5;
  z-index: 0;
  height: 100%;
  width: 100%;
}

/* General dark mode colors */
body {
  background-color: #121212; /* Dark background */
  color: #e0e0e0; /* Light text */
}

/* Ensure content sections are properly positioned */
#hero {
  min-height: 100vh;
  width: 100%;
}

/* Section borders for better visibility in dark mode */
.border {
  border-color: rgba(255, 255, 255, 0.2);
}
</style>
