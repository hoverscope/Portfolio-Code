<template>
  <div
    ref="fadeInElement"
    :class="['fade-in-on-scroll', { 'fade-in': isVisible }]"
  >
    <slot />
  </div>
</template>

<script>
export default {
  name: "FadeInOnScroll",
  data() {
    return {
      isVisible: false,
    };
  },
  mounted() {
    const observer = new IntersectionObserver(
      ([entry]) => {
        if (entry.isIntersecting) {
          this.isVisible = true; // Trigger fade-in when element enters view
        } else {
          this.isVisible = false; // Reset fade-out when element leaves view
        }
      },
      { threshold: 0.3 } // Trigger when 30% of the element is visible
    );
    observer.observe(this.$refs.fadeInElement);
  },
};
</script>

<style scoped>
.fade-in-on-scroll {
  opacity: 0;
  transition: opacity 1s ease-in-out;
}

.fade-in {
  opacity: 1;
}
</style>
