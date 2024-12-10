<script lang="ts">
  import { projects } from '$lib/data/projects';
</script>

<section class="py-16 bg-white" id="projects">
  <div class="container mx-auto px-6">
    <h2 class="text-3xl font-bold mb-8 text-gray-900">Featured Projects</h2>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-8">
      {#each projects as project}
        <div class="group relative aspect-square rounded-xl overflow-hidden shadow-lg">
          <img
            src={project.image}
            alt={project.title}
            class="w-full h-full object-cover transition-all duration-500 group-hover:scale-110 group-hover:rotate-3"
          />
          <div class="absolute inset-0 bg-gradient-to-t from-black/95 via-black/75 to-black/40 opacity-0 group-hover:opacity-100 transition-opacity duration-300">
            <div class="absolute bottom-0 left-0 right-0 p-6">
              <h3 class="text-xl font-semibold text-white mb-2">{project.title}</h3>
              <p class="text-sm text-white/90 mb-4">{project.description}</p>
              <div class="flex flex-wrap gap-2">
                {#each project.platforms as platform}
                  <span class="inline-block px-3 py-1 bg-white/30 backdrop-blur-sm rounded-full text-xs font-medium text-white">
                    {platform}
                  </span>
                {/each}
              </div>
            </div>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>