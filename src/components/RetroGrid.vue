<template>
  <div
    class="pointer-events-none absolute size-full overflow-hidden [perspective:200px]"
    :style="gridStyles"
  >
    <div class="absolute inset-0 [transform:rotateX(var(--grid-angle))]">
      <div
        class="animate-grid [background-image:linear-gradient(to_right,var(--light-line)_1px,transparent_0),linear-gradient(to_bottom,var(--light-line)_1px,transparent_0)] [background-repeat:repeat] [background-size:var(--cell-size)_var(--cell-size)] [height:300vh] [inset:0%_0px] [margin-left:-200%] [transform-origin:100%_0_0] [width:600vw] dark:[background-image:linear-gradient(to_right,var(--dark-line)_1px,transparent_0),linear-gradient(to_bottom,var(--dark-line)_1px,transparent_0)]"
      />
    </div>

    <div class="absolute inset-0" />
  </div>
</template>

<script>
export default {
  name: "RetroGrid",
  props: {
    className: {
      type: String,
      default: "",
    },
    angle: {
      type: Number,
      default: 65,
    },
    cellSize: {
      type: Number,
      default: 60,
    },
    opacity: {
      type: Number,
      default: 0.5,
    },
    lightLineColor: {
      type: String,
      default: "gray",
    },
    darkLineColor: {
      type: String,
      default: "gray",
    },
  },
  computed: {
    gridStyles() {
      return {
        "--grid-angle": `${this.angle}deg`,
        "--cell-size": `${this.cellSize}px`,
        "--opacity": this.opacity,
        "--light-line": this.lightLineColor,
        "--dark-line": this.darkLineColor,
      };
    },
  },
};
</script>

<style scoped>
@keyframes grid {
  0% {
    transform: translateY(-50%);
  }
  100% {
    transform: translateY(0);
  }
}

@tailwind base;
@tailwind components;
@tailwind utilities;

@layer utilities {
  .animate-grid {
    animation: grid 15s linear infinite;
  }
}
</style>
