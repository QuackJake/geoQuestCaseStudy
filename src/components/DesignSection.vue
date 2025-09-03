<template>
  <section id="design" class="py-16 px-6 bg-muted/30">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-4xl font-bold text-primary mb-12 text-center">Final Design</h2>
      <div class="grid md:grid-cols-2 gap-8 mb-12">
        <div 
          v-for="feature in designFeatures" 
          :key="feature.title"
          class="bg-card p-6 rounded-lg shadow-sm border border-border"
        >
          <h3 class="text-xl font-semibold text-card-foreground mb-3">{{ feature.title }}</h3>
          <p class="text-muted-foreground leading-relaxed mb-4">{{ feature.description }}</p>
          <div class="flex flex-wrap gap-2">
            <span 
              v-for="tag in feature.tags" 
              :key="tag"
              class="bg-primary/10 text-primary px-3 py-1 rounded-full text-sm"
            >
              {{ tag }}
            </span>
          </div>
        </div>
      </div>
      
      <div class="bg-card rounded-lg p-8 text-center border border-border">
        <div class="bg-gradient-to-br from-primary/10 to-accent/10 rounded-lg p-12 mb-6">
          <span class="text-8xl">🎨</span>
          <p class="text-muted-foreground mt-4">Interactive prototype and high-fidelity mockups</p>
        </div>
        <button class="bg-primary text-primary-foreground px-6 py-3 rounded-lg font-semibold hover:bg-primary/90 transition-colors duration-200">
          View Live Prototype
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
defineProps({
  designFeatures: Array
})
</script>