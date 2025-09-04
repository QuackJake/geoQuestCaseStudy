<script setup>
import Header from './components/Header.vue'
import Introduction from './components/Introduction.vue'
import Research from './components/Research.vue'
import Design from './components/Design.vue'
import WireframeGallery from './components/galleries/WireframeGallery.vue'
import UserTesting from './components/UserTesting.vue'
import FinalProduct from './components/FinalProduct.vue'
import PrototypeGallery from './components/galleries/PrototypeGallery.vue'
import Reflection from './components/Reflection.vue'
import Footer from './components/Footer.vue'

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
      <WireframeGallery />
      <UserTesting />
      <FinalProduct />
      <PrototypeGallery />
      <Reflection />
    </main>
    <Footer />
  </div>
</template>
