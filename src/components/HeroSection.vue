<template>
  <section id="introduction" class="pt-24 pb-16 px-6">
    <div class="max-w-4xl mx-auto text-center">
      <h1 class="text-5xl md:text-6xl font-bold text-primary mb-6 text-balance">
        Application Design Process
      </h1>
      <p class="text-xl text-muted-foreground mb-8 text-pretty leading-relaxed max-w-2xl mx-auto">
        A comprehensive case study showcasing my systematic approach to creating user-centered digital experiences through research, iteration, and thoughtful design decisions.
      </p>
      <button 
        @click="$emit('scrollTo', 'research')"
        class="bg-accent text-accent-foreground px-8 py-3 rounded-lg font-semibold hover:bg-accent/90 transition-colors duration-200"
      >
        Explore the Process
      </button>
    </div>
  </section>
</template>