<template>
  <!-- ================= User Testing Section ================= -->
  <section id="userTesting" class="py-16 px-6 bg-muted/5">
    <div class="max-w-6xl mx-auto">

      <!-- ===== Title ===== -->
      <h2 class="my-16 text-4xl font-bold text-primary text-center">
        User Testing & Implementation
      </h2>

      <!-- ===== Introduction / Testing Goal ===== -->
      <div class="flex flex-col justify-center text-center max-w-3xl mx-auto">
        <p class="text-muted-foreground leading-relaxed">
          Our usability testing plan was designed to gather genuine, comprehensive feedback from diverse users. 
          By keeping instructions vague and open-ended, we encouraged participants to explore freely, describe their interpretations, and highlight pain points.
        </p>
      </div>

      <!-- ===== Testing Process Steps ===== -->
      <div>
        <div
          v-for="(step, index) in processSteps"
          :key="step.title"
          :class="[
            'flex flex-col md:flex-row items-center gap-8 min-h-[50vh]',
            index % 2 === 1 ? 'md:flex-row-reverse' : ''
          ]"
        >
          <!-- Step Content -->
          <div class="flex-1 flex flex-col justify-center">
            <div class="flex items-center mb-4">
              <h3 class="text-2xl font-semibold text-foreground">
                {{ step.title }}
              </h3>
            </div>
            <p class="text-muted-foreground leading-relaxed mb-4">
              {{ step.description }}
            </p>

            <!-- Deliverables / Key Artifacts -->
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
          <div class="flex-1 flex flex-col justify-center">
            <div class="bg-muted/50 rounded-lg p-8 text-center h-full flex flex-col justify-center">
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

      <!-- ===== Key Insights & Implemented Changes Side-by-Side ===== -->
      <div class="mt-12 flex flex-col md:flex-row gap-12">
        
        <!-- Key User Insights -->
        <div class="flex-1 flex flex-col justify-start">
          <h3 class="text-3xl font-semibold text-primary mb-6 text-center md:text-left">
            Key Insights from Testing
          </h3>
          <ul class="space-y-4 text-muted-foreground">
            <li>Users expressed confusion over certain UI elements like "hamburger" menu, "coins", and camera icon.</li>
            <li>Open-ended walkthroughs prompted detailed screen descriptions and interpretations, highlighting usability issues.</li>
            <li>Participants provided concrete suggestions, such as adding a dedicated "find quests around you" button.</li>
            <li>Diverse user roles ensured feedback captured a broad spectrum of perspectives.</li>
          </ul>
        </div>

        <!-- Implemented Changes -->
        <div class="flex-1 flex flex-col justify-start">
          <h3 class="text-3xl font-semibold text-primary mb-6 text-center md:text-left">
            How Feedback Shaped the Design
          </h3>
          <p class="text-muted-foreground leading-relaxed">
            Insights from testing guided refinements to navigation, labeling, and quest discovery features. 
            Confusing icons were clarified, and screens were adjusted to better align with user expectations, ensuring a smoother and more intuitive app experience.
          </p>
        </div>

      </div>

    </div>
  </section>
</template>

<script setup>
import placeholder from '../assets/taylorSS.png'
import notebookLM from '../assets/notebookLM.png'
const processSteps = [
  {
    title: 'Research',
    description:
      'Gathered insights through user interviews, competitive analysis, and surveys to identify core user needs and pain points.',
    deliverables: ['User Personas', 'Survey Results', 'Competitive Analysis'],
    image: placeholder,
    visualDescription: 'Usability Test Recordings'
  },
  {
    title: 'Ideation',
    description:
      'Brainstormed multiple design directions and mapped out user flows to ensure alignment with user goals and business objectives.',
    deliverables: ['Storyboards', 'User Flows', 'Sketches'],
    image: notebookLM,
    visualDescription: 'LLM-Assisted Ideation (NotebookLM)'
  }
]
</script>
