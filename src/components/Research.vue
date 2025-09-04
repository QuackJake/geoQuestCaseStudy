<script setup lang="tsx">
</script>

<template>
  <!-- ================= Research Section ================= -->
  <section id="research" class="py-20 px-6 bg-muted/30">
    <div class="max-w-6xl mx-auto">
      <!-- ===== Section Title ===== -->
      <h2 class="text-4xl md:text-5xl font-bold text-primary mb-12 text-center leading-snug">
        Research & Insights
      </h2>

      <!-- ===== Research Items ===== -->
      <div class="flex flex-col gap-20">

        <!-- ===== User Personas ===== -->
        <div class="flex flex-col md:flex-row items-center gap-10">
          <!-- Image -->
          <img 
            src="../assets/persona.jpg" 
            alt="User Persona Illustration" 
            class="w-full md:w-1/2 rounded-lg shadow-lg"
          />
          <!-- Text -->
          <div class="md:w-1/2">
            <h3 class="text-3xl font-semibold text-primary mb-4">User Personas</h3>
            <p class="text-lg text-muted-foreground leading-relaxed">
              Personas represent the key user groups for this application. By understanding their
              needs, goals, and pain points, we were able to design features that deliver real value
              and improve user experience.
            </p>
          </div>
        </div>

        <!-- ===== Story Maps ===== -->
        <div class="flex flex-col md:flex-row items-center gap-10 md:flex-row-reverse">
          <!-- Image -->
          <img 
            src="../assets/story-map.jpg" 
            alt="Story Map Illustration" 
            class="w-full md:w-1/2 rounded-lg shadow-lg"
          />
          <!-- Text -->
          <div class="md:w-1/2">
            <h3 class="text-3xl font-semibold text-primary mb-4">Story Maps</h3>
            <p class="text-lg text-muted-foreground leading-relaxed">
              Story mapping helps visualize the user journey and identify high-priority features.
              It allowed us to align development efforts with user needs, ensuring a coherent flow
              from onboarding to advanced tasks.
            </p>
          </div>
        </div>

        <!-- ===== User Flows ===== -->
        <div class="flex flex-col md:flex-row items-center gap-10">
          <!-- Image -->
          <img 
            src="../assets/user-flow.jpg" 
            alt="User Flow Diagram" 
            class="w-full md:w-1/2 rounded-lg shadow-lg"
          />
          <!-- Text -->
          <div class="md:w-1/2">
            <h3 class="text-3xl font-semibold text-primary mb-4">User Flows</h3>
            <p class="text-lg text-muted-foreground leading-relaxed">
              User flows illustrate the step-by-step paths users take to complete tasks within the
              application. This helped identify friction points and optimize the navigation for a
              smoother experience.
            </p>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>
