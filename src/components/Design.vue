<template>
  <!-- ================= Section: Design Evolution ================= -->
  <section id="design" class="py-20 px-6 bg-muted/30">
    <div class="max-w-6xl mx-auto">

      <!-- ===== Section Title ===== -->
      <h2 class="text-4xl md:text-5xl font-bold text-primary mb-16 text-center leading-snug">
        Design Evolution
      </h2>

      <!-- ===== Design Features Grid ===== -->
      <div class="grid md:grid-cols-2 gap-12 mb-16">
        <div
          v-for="feature in designFeatures"
          :key="feature.title"
          class="bg-card p-6 rounded-lg shadow-md border border-border flex flex-col"
        >
          <!-- Feature Image -->
          <img
            :src="feature.image || placeholder"
            :alt="feature.title"
            class="w-full h-48 md:h-56 object-cover rounded-md mb-4"
          />

          <!-- Feature Title -->
          <h3 class="text-2xl font-semibold text-card-foreground mb-3">
            {{ feature.title }}
          </h3>

          <!-- Feature Description -->
          <p class="text-lg text-muted-foreground leading-relaxed mb-4 flex-1">
            {{ feature.description }}
          </p>

          <!-- Tags -->
          <div class="flex flex-wrap gap-2 mt-auto">
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

      <!-- ===== Prototype Callout ===== -->
      <div class="bg-card rounded-lg p-8 text-center border border-border">
        <div class="bg-gradient-to-br from-primary/10 to-accent/10 rounded-lg p-12 mb-6 flex flex-col items-center">
          <img
            :src="placeholder"
            alt="Prototype preview"
            class="w-32 h-32 object-cover rounded-lg mb-4"
          />
          <p class="text-lg text-muted-foreground text-center">
            Interactive prototype and high-fidelity mockups
          </p>
        </div>
        <button
          class="bg-primary text-primary-foreground px-8 py-3 rounded-lg font-semibold hover:bg-primary/90 transition-colors duration-200"
        >
          View Live Prototype
        </button>
      </div>

    </div>
  </section>
</template>

<script setup>
import placeholder from '../assets/placeholder.jpg'

const designFeatures = [
  {
    title: 'Color Palette & Typography',
    description:
      'Established a consistent color scheme and typography hierarchy to ensure visual clarity and brand cohesion across the application.',
    tags: ['Colors', 'Typography', 'Branding'],
    image: placeholder
  },
  {
    title: 'Wireframes',
    description:
      'Low-fidelity wireframes created to explore layout options, component placement, and overall user flow before high-fidelity design.',
    tags: ['Wireframes', 'UX', 'Layout'],
    image: placeholder
  },
  {
    title: 'Usability Considerations',
    description:
      'Iterative testing and feedback incorporated to ensure accessibility, intuitive navigation, and minimal cognitive load.',
    tags: ['Usability', 'Accessibility', 'Testing'],
    image: placeholder
  },
  {
    title: 'Final Design',
    description:
      'High-fidelity screens with polished UI components, consistent spacing, and interactive elements to enhance user experience.',
    tags: ['UI', 'High-Fidelity', 'Interaction'],
    image: placeholder
  }
]
</script>
