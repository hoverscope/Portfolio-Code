<template>
  <section id="work" class="text-white relative pt-0">
    <!-- Work experience content container -->
    <div class="max-w-6xl mx-auto text-right px-4 sm:px-6 md:px-8">
      <h2
        class="text-3xl font-extrabold sm:text-4xl md:text-5xl lg:text-6xl xl:text-6xl mb-6"
      >
        Work Experience
      </h2>

      <!-- Work Experience Entry -->
      <div
        class="bg-gray-800 rounded-lg mb-6 overflow-hidden transition-all duration-300"
        :class="{ 'shadow-lg': activeEntry === 1 }"
      >
        <div
          class="flex items-center justify-between p-6 flex-col sm:flex-row cursor-pointer transition-colors"
          @click="toggleEntry(1)"
        >
          <!-- Circle on the left -->
          <div
            class="w-16 h-16 bg-blue-500 rounded-full flex items-center justify-center text-white font-bold text-lg mb-4 sm:mb-0"
          >
            <span>1</span>
          </div>

          <!-- Name and Position -->
          <div class="flex-1 ml-4 flex flex-col items-start sm:items-start">
            <h3 class="text-xl font-semibold">Software Developer Intern</h3>
            <p class="text-sm text-gray-400">Inlogic IT Solutions</p>
          </div>

          <!-- Time and expand icon -->
          <div class="flex-shrink-0 mt-4 sm:mt-0 flex items-center gap-3">
            <span class="text-gray-400">June - August 2024</span>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-5 w-5 transform transition-transform duration-300"
              :class="{ 'rotate-180': activeEntry === 1 }"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M19 9l-7 7-7-7"
              />
            </svg>
          </div>
        </div>

        <!-- Expandable Content -->
        <div
          class="overflow-hidden transition-all duration-300"
          :style="{ maxHeight: activeEntry === 1 ? '500px' : '0px' }"
        >
          <div class="p-6 pt-0 text-left bg-gray-750">
            <ul class="list-disc list-inside space-y-2 text-gray-300">
              <li>
                Developed and maintained web applications using .NET, C# and
                Javascript.
              </li>
              <li>
                Implemented responsive UI designs and improved user experience
              </li>
              <li>
                Collaborated with the team on API integration and database
                management with MS SQL Server.
              </li>
              <li>
                Participated in code reviews and agile development processes
                while working closely with senior developers.
              </li>
            </ul>
          </div>
        </div>
      </div>

      <!-- Second Work Experience Entry -->
      <div
        class="bg-gray-800 rounded-lg mb-6 overflow-hidden transition-all duration-300"
        :class="{ 'shadow-lg': activeEntry === 2 }"
      >
        <div
          class="flex items-center justify-between p-6 flex-col sm:flex-row cursor-pointer transition-colors"
          @click="toggleEntry(2)"
        >
          <!-- Circle on the left -->
          <div
            class="w-16 h-16 bg-green-500 rounded-full flex items-center justify-center text-white font-bold text-lg mb-4 sm:mb-0"
          >
            <span>2</span>
          </div>

          <!-- Name and Position -->
          <div class="flex-1 ml-4 flex flex-col items-start sm:items-start">
            <h3 class="text-xl font-semibold">ML & Data Analyst Intern</h3>
            <p class="text-sm text-gray-400">Labware LIMS</p>
          </div>

          <!-- Time and expand icon -->
          <div class="flex-shrink-0 mt-4 sm:mt-0 flex items-center gap-3">
            <span class="text-gray-400">May - October 2023</span>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-5 w-5 transform transition-transform duration-300"
              :class="{ 'rotate-180': activeEntry === 2 }"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M19 9l-7 7-7-7"
              />
            </svg>
          </div>
        </div>

        <!-- Expandable Content -->
        <div
          class="overflow-hidden transition-all duration-300"
          :style="{ maxHeight: activeEntry === 2 ? '500px' : '0px' }"
        >
          <div class="p-6 pt-0 text-left bg-gray-750">
            <ul class="list-disc list-inside space-y-2 text-gray-300">
              <li>Analyzed large datasets using Python and ML libraries</li>
              <li>Developed predictive models for data analysis</li>
              <li>Created data visualization dashboards</li>
              <li>
                Optimized database queries and improved data processing
                efficiency with SQL server
              </li>
              <li>Worked width Flask, Javascript and Express API</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      activeEntry: null,
    };
  },
  methods: {
    toggleEntry(entryId) {
      this.activeEntry = this.activeEntry === entryId ? null : entryId;
    },
  },
};
</script>

<style scoped>
/* Base styles */
section {
  margin: 0;
}

#work {
  width: 100%;
  margin-top: 12rem;
}

#work .max-w-6xl {
  text-align: right;
}

#work .w-16 {
  width: 4rem;
  height: 4rem;
}

#work .bg-blue-500 {
  background-color: #3b82f6;
}

#work .flex-col.items-start {
  text-align: left;
}

/* Background color for expanded content */
.bg-gray-750 {
  background-color: rgba(31, 41, 55, 0.5);
}

/* Responsive styles */
@media (min-width: 640px) {
  #work .flex-col.sm\:flex-row {
    flex-direction: row;
  }

  #work .sm\:mt-0 {
    margin-top: 0;
  }

  #work .sm\:items-start {
    align-items: flex-start;
  }

  #work .sm\:mb-0 {
    margin-bottom: 0;
  }
}
</style>
