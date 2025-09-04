<template>
  <!-- ================= Process Section ================= -->
  <section id="userTesting" class="py-16 px-6">
    <div class="max-w-6xl mx-auto">

      <!-- ===== Title ===== -->
      <h2 class="text-4xl font-bold text-primary mb-12 text-center">
        User Testing Conclusions
      </h2>

      <!-- ===== Steps ===== -->
      <div class="space-y-12">
        <div
          v-for="(step, index) in processSteps"
          :key="step.title"
          :class="[
            'flex flex-col md:flex-row items-center gap-8',
            index % 2 === 1 ? 'md:flex-row-reverse' : ''
          ]"
        >
          <!-- Step Content -->
          <div class="flex-1">
            <div class="flex items-center mb-4">
              <span class="bg-accent text-accent-foreground w-8 h-8 rounded-full flex items-center justify-center font-bold mr-4">
                {{ index + 1 }}
              </span>
              <h3 class="text-2xl font-semibold text-foreground">
                {{ step.title }}
              </h3>
            </div>
            <p class="text-muted-foreground leading-relaxed mb-4">
              {{ step.description }}
            </p>

            <!-- Deliverables -->
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

          <!-- Step Visual -->
          <div class="flex-1">
            <div class="bg-muted/50 rounded-lg p-8 text-center">
              <img
                :src="step.image || placeholder"
                :alt="step.title"
                class="w-full h-48 object-cover rounded-md mb-4"
              />
              <p class="text-sm text-muted-foreground">
                {{ step.visualDescription }}
              </p>
            </div>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
/* ================= Imports ================= */
import placeholder from '../assets/placeholder.jpg'

/* ================= Local Data ================= */
const processSteps = [
  {
    title: 'Research',
    description:
      'Gathered insights through user interviews, competitive analysis, and surveys to identify core user needs and pain points.',
    deliverables: ['User Personas', 'Survey Results', 'Competitive Analysis'],
    image: placeholder,
    visualDescription: 'Research artifacts and findings'
  },
  {
    title: 'Ideation',
    description:
      'Brainstormed multiple design directions and mapped out user flows to ensure alignment with user goals and business objectives.',
    deliverables: ['Storyboards', 'User Flows', 'Sketches'],
    image: placeholder,
    visualDescription: 'Concept sketches and flows'
  },
  {
    title: 'Prototyping',
    description:
      'Built interactive wireframes and low-fidelity prototypes to validate ideas early with stakeholders and users.',
    deliverables: ['Wireframes', 'Low-fi Prototype'],
    image: placeholder,
    visualDescription: 'Wireframe examples'
  },
  {
    title: 'Testing',
    description:
      'Conducted usability tests to refine interactions, address usability issues, and improve overall user satisfaction.',
    deliverables: ['Usability Findings', 'Refined Flows'],
    image: placeholder,
    visualDescription: 'Testing session highlights'
  }
]
</script>
