<script lang="ts">
  import { Github, Linkedin, Mail } from 'lucide-svelte';
</script>

<header class="relative overflow-hidden">
  <div class="absolute inset-0 bg-gradient-to-br from-purple-800 to-blue-400 opacity-98"></div>
  <div class="relative container mx-auto px-6 py-16 md:py-24">
    <div class="flex flex-col md:flex-row items-center gap-8">
      <div class="w-48 h-48 rounded-full overflow-hidden bg-white/20 flex-shrink-0 ring-4 ring-white/30">
        <img
          src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?fit=crop&w=400&h=400"
          alt="Profile placeholder"
          class="w-full h-full object-cover"
        />
      </div>
      <div class="text-center md:text-left">
        <h1 class="text-4xl md:text-5xl font-bold text-white mb-4 drop-shadow-lg">Seth Johnson</h1>
        <h2 class="text-2xl md:text-3xl text-white mb-6 drop-shadow">Software Development & Technology Leadership</h2>
        <div class="flex gap-4 justify-center md:justify-start">
          <a
            href="https://www.linkedin.com/in/gotosethj/"
            target="_blank"
            rel="noopener noreferrer"
            class="bg-white/20 hover:bg-white/30 p-3 rounded-full transition-colors ring-2 ring-white/30"
          >
            <Linkedin class="w-6 h-6 text-white" />
          </a>
          <a
            href="https://github.com"
            target="_blank"
            rel="noopener noreferrer"
            class="bg-white/20 hover:bg-white/30 p-3 rounded-full transition-colors ring-2 ring-white/30"
          >
            <Github class="w-6 h-6 text-white" />
          </a>
          <a
            href="mailto:example@email.com"
            class="bg-white/20 hover:bg-white/30 p-3 rounded-full transition-colors ring-2 ring-white/30"
          >
            <Mail class="w-6 h-6 text-white" />
          </a>
        </div>
      </div>
    </div>
  </div>
</header>