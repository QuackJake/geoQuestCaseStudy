<template>
  <section id="process" class="py-16 px-6">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-4xl font-bold text-primary mb-12 text-center">Design Process</h2>
      <div class="space-y-12">
        <div 
          v-for="(step, index) in processSteps" 
          :key="step.title"
          :class="[
            'flex flex-col md:flex-row items-center gap-8',
            index % 2 === 1 ? 'md:flex-row-reverse' : ''
          ]"
        >
          <div class="flex-1">
            <div class="flex items-center mb-4">
              <span class="bg-accent text-accent-foreground w-8 h-8 rounded-full flex items-center justify-center font-bold mr-4">
                {{ index + 1 }}
              </span>
              <h3 class="text-2xl font-semibold text-foreground">{{ step.title }}</h3>
            </div>
            <p class="text-muted-foreground leading-relaxed mb-4">{{ step.description }}</p>
            <ul class="space-y-2">
              <li 
                v-for="deliverable in step.deliverables" 
                :key="deliverable"
                class="flex items-center text-sm text-muted-foreground"
              >
                <span class="w-2 h-2 bg-accent rounded-full mr-3"></span>
                {{ deliverable }}
              </li>
            </ul>
          </div>
          <div class="flex-1">
            <div class="bg-muted/50 rounded-lg p-8 text-center">
              <span class="text-6xl">{{ step.visual }}</span>
              <p class="text-sm text-muted-foreground mt-4">{{ step.visualDescription }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
defineProps({
  processSteps: Array
})
</script>