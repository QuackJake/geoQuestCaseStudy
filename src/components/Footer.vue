<template>
  <footer class="py-12 px-6"
    style="background: linear-gradient(to right, #D0F3FD, #8183DD);">
    <div class="max-w-6xl mx-auto flex flex-col md:flex-row items-center justify-between gap-8">

      <!-- CTA Section -->
      <div class="text-center md:text-left flex-1">
        <h3 class="text-2xl font-semibold mb-2">Let's Create Something Amazing</h3>
        <p class="tmb-4">
          Interested in working together? I'd love to hear about your next project.
        </p>
        <a 
          href="mailto:your.email@example.com"
          class="inline-block bg-accent text-accent-foreground px-6 py-3 rounded-lg font-semibold hover:bg-accent/90 transition-colors duration-200"
        >
          Get In Touch
        </a>
      </div>

      <!-- Social Links Section -->
      <div class="flex flex-col items-center md:items-end gap-4">
        <h4 class="text-lg font-medium mb-2">Connect with me</h4>
        <div class="flex gap-4">
          <!-- GitHub -->
          <a 
            href="https://github.com/QuackJake" 
            target="_blank" 
            rel="noopener noreferrer"
            class="hover:text-accent transition-colors duration-200"
            aria-label="GitHub"
          >
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M12 0.297C5.373 0.297 0 5.67 0 12.297c0 5.292 3.438 9.79 8.207 11.387.6.111.793-.261.793-.579 0-.287-.011-1.244-.017-2.255-3.338.726-4.042-1.612-4.042-1.612-.546-1.387-1.333-1.756-1.333-1.756-1.089-.744.083-.729.083-.729 1.205.085 1.839 1.238 1.839 1.238 1.07 1.834 2.807 1.304 3.492.997.108-.774.419-1.304.762-1.604-2.665-.303-5.466-1.333-5.466-5.933 0-1.311.469-2.382 1.236-3.222-.124-.303-.536-1.524.117-3.176 0 0 1.008-.322 3.301 1.23a11.53 11.53 0 013.003-.404c1.018.005 2.042.138 3.003.404 2.291-1.552 3.297-1.23 3.297-1.23.656 1.652.244 2.873.12 3.176.77.84 1.235 1.911 1.235 3.222 0 4.61-2.807 5.625-5.479 5.921.43.37.815 1.102.815 2.222 0 1.604-.015 2.897-.015 3.293 0 .321.192.694.8.576C20.565 22.082 24 17.584 24 12.297c0-6.627-5.373-12-12-12z"/>
            </svg>
          </a>

          <!-- LinkedIn -->
          <a 
            href="https://www.linkedin.com/in/jake-quackenbush-1b2997256/" 
            target="_blank" 
            rel="noopener noreferrer"
            class="hover:text-accent transition-colors duration-200"
            aria-label="LinkedIn"
          >
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M4.98 3.5C4.98 4.88 3.88 6 2.5 6S0 4.88 0 3.5 1.12 1 2.5 1s2.48 1.12 2.48 2.5zM.22 8.03h4.55V24H.22V8.03zM8.98 8.03h4.37v2.16h.06c.61-1.16 2.1-2.38 4.32-2.38 4.62 0 5.47 3.05 5.47 7.01V24h-4.55v-7.4c0-1.76-.03-4.03-2.46-4.03-2.46 0-2.84 1.93-2.84 3.92V24H8.98V8.03z"/>
            </svg>
          </a>

          <!-- Email -->
          <a 
            href="mailto:jake.qbushed@gmail.com"
            class="hover:text-accent transition-colors duration-200"
            aria-label="Email"
          >
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M20 4H4C2.895 4 2 4.895 2 6v12c0 1.105.895 2 2 2h16c1.105 0 2-.895 2-2V6c0-1.105-.895-2-2-2zm0 2v.511l-8 5.011-8-5.011V6h16zm-16 12V9.489l7.555 4.722c.185.116.394.174.61.174s.425-.058.61-.174L20 9.489V18H4z"/>
            </svg>
          </a>
        </div>
      </div>

    </div>

    <!-- ===== Footer Bottom ===== -->
    <div class="mt-12 border-t border-primary-foreground/20 pt-6 text-center text-sm">
      &copy; 2025 Jake Quackenbush. All rights reserved.
    </div>
  </footer>
</template>
