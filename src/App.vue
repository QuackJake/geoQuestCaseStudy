<script setup>
import Header from './components/Header.vue'
import Introduction from './components/Introduction.vue'
import Research from './components/Research.vue'
import Design from './components/Design.vue'
import Carousel from './galleries/Carousel.vue'
import UserTesting from './components/UserTesting.vue'
import FinalProduct from './components/FinalProduct.vue'
import Reflection from './components/Reflection.vue'
import Footer from './components/Footer.vue'

const wireframes = [
  { id: 1, url: new URL('assets/wireframes/clickQuest.png', import.meta.url).href },
  { id: 2, url: new URL('assets/wireframes/coins.png', import.meta.url).href },
  { id: 3, url: new URL('assets/wireframes/homePage.png', import.meta.url).href },
  { id: 4, url: new URL('assets/wireframes/questCost.png', import.meta.url).href },
  { id: 5, url: new URL('assets/wireframes/questStart.png', import.meta.url).href },
  { id: 6, url: new URL('assets/wireframes/submitImage.png', import.meta.url).href },
];

const mockups = [
  { id: 1, url: new URL('assets/mockups/homeScreen.png', import.meta.url).href },
  { id: 2, url: new URL('assets/mockups/inventory.png', import.meta.url).href },
  { id: 3, url: new URL('assets/mockups/quest.png', import.meta.url).href },
  { id: 4, url: new URL('assets/mockups/placeQuest.png', import.meta.url).href },
  { id: 5, url: new URL('assets/mockups/questAdded.png', import.meta.url).href },
  { id: 6, url: new URL('assets/mockups/questStarted.png', import.meta.url).href },
];

const scrollTo = (id) => {
  const el = document.getElementById(id)
  if (el) {
    el.scrollIntoView({ behavior: 'smooth' })
  }
}
</script>

<template>
  <div class="min-h-screen bg-background text-foreground">
    <Header @scrollTo="scrollTo" />
    <main>
      <Introduction @scrollTo="scrollTo" />
      <Research />
      <Design   />
      <Carousel :images="wireframes" header="Wireframes"/>
      <UserTesting />
      <FinalProduct />
      <Carousel :images="mockups" header="FinalMockups"/>
      <Reflection />
    </main>
    <Footer />
  </div>
</template>
