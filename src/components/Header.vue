<template>
  <!-- ================= Header ================= -->
  <header
    :class="[
      'fixed top-0 left-0 right-0 z-50 transition-all duration-300',
      scrolled ? 'bg-background/95 border-b border-border/40 backdrop-blur' : 'bg-transparent'
    ]"
  >
    <div class="max-w-6xl mx-auto flex h-16 items-center justify-between px-6">

      <div class="flex items-center space-x-2">
        <div class="h-8 w-8 rounded-lg bg-primary"></div>
        <span class="font-bold text-lg">GeoQuest</span>
      </div>

      <nav class="hidden md:flex space-x-8">
        <button
          v-for="link in links"
          :key="link.id"
          @click="scrollTo(link.id)"
          class="text-sm font-medium transition-colors hover:text-primary"
        >
          {{ link.label }}
        </button>
      </nav>

      <button
        class="md:hidden p-2 rounded-lg hover:bg-muted"
        @click="menuOpen = !menuOpen"
      >
        <svg
          v-if="!menuOpen"
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
            d="M4 6h16M4 12h16M4 18h16" />
        </svg>

        <svg
          v-else
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
            d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
    </div>

    <div
      v-if="menuOpen"
      class="md:hidden bg-background border-t border-border/40 px-6 py-4 space-y-4"
    >
      <button
        v-for="link in links"
        :key="link.id"
        @click="scrollTo(link.id, true)"
        class="block w-full text-left font-medium text-muted-foreground hover:text-primary"
      >
        {{ link.label }}
      </button>
    </div>
  </header>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'

const links = [
  { id: 'research', label: 'Research' },
  { id: 'design', label: 'Design' },
  { id: 'userTesting', label: 'User Testing' },
  { id: 'finalProduct', label: 'Final Product' },
]

const menuOpen = ref(false)
const scrolled = ref(false)

const handleScroll = () => {
  scrolled.value = window.scrollY > 10
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onBeforeUnmount(() => {
  window.removeEventListener('scroll', handleScroll)
})

const scrollTo = (id, closeMenu = false) => {
  if (closeMenu) menuOpen.value = false
  const el = document.getElementById(id)
  if (el) el.scrollIntoView({ behavior: 'smooth' })
}
</script>
