<template>
  <section id="conclusion" class="py-16 px-6">
    <div class="max-w-4xl mx-auto text-center">
      <h2 class="text-4xl font-bold text-primary mb-8">Key Learnings & Impact</h2>
      <div class="grid md:grid-cols-3 gap-8 mb-12">
        <div 
          v-for="metric in metrics" 
          :key="metric.label"
          class="text-center"
        >
          <div class="text-3xl font-bold text-accent mb-2">{{ metric.value }}</div>
          <div class="text-muted-foreground">{{ metric.label }}</div>
        </div>
      </div>
      <p class="text-lg text-muted-foreground leading-relaxed mb-8 text-pretty">
        This project reinforced the importance of user-centered design and iterative testing. 
        The systematic approach to research and validation resulted in a solution that not only 
        met business objectives but genuinely improved the user experience.
      </p>
      <button class="bg-accent text-accent-foreground px-8 py-3 rounded-lg font-semibold hover:bg-accent/90 transition-colors duration-200">
        View Next Case Study
      </button>
    </div>
  </section>
</template>

<script setup>
defineProps({
  metrics: Array
})
</script>