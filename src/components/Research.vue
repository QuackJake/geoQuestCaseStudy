<script setup lang="tsx">
</script>

<template>
  <!-- ================= Research Section ================= -->
  <section id="research" class="py-20 px-6 bg-muted/30"
    style="background: linear-gradient(to right, #D0F3FD, #8183DD);">
    <div class="max-w-6xl mx-auto">
      
      <h2 class="text-4xl md:text-5xl font-bold text-primary mb-12 text-center leading-snug">
        Research & Insights
      </h2>

      <div class="flex flex-col gap-20">
        <!-- User Personas -->
        <div class="flex flex-col md:flex-row items-center gap-10">
          <div class="w-full md:w-1/2">
            <div class="aspect-w-16 aspect-h-9 rounded-lg overflow-hidden shadow-lg">
              <img 
                src="../assets/cindyLee.png" 
                alt="User Persona Illustration" 
                class="object-cover w-full h-full"
              />
            </div>
          </div>
          <div class="w-full md:w-1/2">
            <h3 class="text-3xl font-semibold text-primary mb-4">User Personas</h3>
            <p class="text-lg text-muted-foreground leading-relaxed">
              Personas represent the key user groups for this application. By understanding their
              needs, goals, and pain points, we were able to design features that deliver real value
              and improve user experience.
            </p>
          </div>
        </div>

        <!-- Story Maps -->
        <div class="flex flex-col md:flex-row items-center gap-10 md:flex-row-reverse">
          <div class="w-full md:w-1/2">
            <div class="aspect-w-16 aspect-h-9 rounded-lg overflow-hidden shadow-lg">
              <img 
                src="../assets/storyMap.png" 
                alt="Story Map Illustration" 
                class="object-cover w-full h-full"
              />
            </div>
          </div>
          <div class="w-full md:w-1/2">
            <h3 class="text-3xl font-semibold text-primary mb-4">Story Maps</h3>
            <p class="text-lg text-muted-foreground leading-relaxed">
              Story mapping helps visualize the user journey and identify high-priority features.
              It allowed us to align development efforts with user needs, ensuring a coherent flow
              from onboarding to advanced tasks.
            </p>
          </div>
        </div>

        <!-- User Flows -->
        <div class="flex flex-col md:flex-row items-center gap-10">
          <div class="w-full md:w-1/2">
            <div class="aspect-w-16 aspect-h-9 rounded-lg overflow-hidden shadow-lg">
              <img 
                src="../assets/userFlows.png" 
                alt="User Flow Diagram" 
                class="object-cover w-full h-full"
              />
            </div>
          </div>
          <div class="w-full md:w-1/2">
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
