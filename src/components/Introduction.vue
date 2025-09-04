<template>
  <!-- ================= Hero / Introduction ================= -->
  <section id="introduction" class="relative h-[70vh] flex items-center justify-center text-center px-6 bg-cover bg-center">
    <div class="max-w-4xl mx-auto" style="background-image: url('/assets/placeholder.jpg');">
      <!-- ===== Title ===== -->
      <h1 class="text-4xl md:text-6xl font-bold text-primary mb-4 leading-snug">
        GeoQuest: A Case Study
      </h1>

      <!-- ===== Subtitle / Description ===== -->
      <p class="text-lg md:text-xl text-muted-foreground leading-relaxed max-w-2xl mx-auto">
        A comprehensive case study showcasing my approach to finding a problem, and solving
        it in a way that build user retention and creates an enjoyable experience for my users
      </p>
    </div>
  </section>

  <!-- ================= Problem Statement ================= -->
  <section id="problem" class="py-16 px-6 flex flex-col md:flex-row items-center max-w-6xl mx-auto gap-8">
    <!-- Problem Image -->
    <img 
      src="../assets/problem-image.jpg" 
      alt="Problem Illustration" 
      class="w-full md:w-1/2 rounded-lg shadow-lg"
    />

    <!-- Problem Text -->
    <div class="md:w-1/2">
      <h2 class="text-3xl font-semibold text-primary mb-4">The Problem</h2>
      <p class="text-lg text-muted-foreground leading-relaxed">
        Clearly define the problem your project is solving. Explain why it matters,
        the pain points users face, and how solving it will improve their experience.
      </p>
    </div>
  </section>
</template>
