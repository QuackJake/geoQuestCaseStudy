<template>
  <div class="min-h-screen bg-background text-foreground">
    <HeaderSection @scrollTo="scrollTo" />
    <main>
      <HeroSection @scrollTo="scrollTo" />
      <ProcessSection :processSteps="processSteps" />
      <DesignSection :designFeatures="designFeatures" />
      <ConclusionSection :metrics="metrics" />
    </main>
    <FooterSection />
  </div>
</template>

<script setup>
import HeaderSection from './components/HeaderSection.vue'
import HeroSection from './components/HeroSection.vue'
import ProcessSection from './components/ProcessSection.vue'
import DesignSection from './components/DesignSection.vue'
import ConclusionSection from './components/ConclusionSection.vue'
import FooterSection from './components/FooterSection.vue'

import processSteps from './data/processSteps.js'
import designFeatures from './data/designFeatures.js'
import metrics from './data/metrics.js'

const scrollTo = (id) => {
  const el = document.getElementById(id)
  if (el) {
    el.scrollIntoView({ behavior: 'smooth' })
  }
}
</script>