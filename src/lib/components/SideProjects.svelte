<script lang="ts">
  import { sideProjects } from '$lib/data/sideProjects';
</script>

<section class="py-16 bg-white" id="side-projects">
  <div class="container mx-auto px-6">
    <h2 class="text-3xl font-bold mb-8 text-gray-900">Side Projects</h2>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-2 sm:gap-6 max-w-7xl mx-auto">
      {#each sideProjects as project}

        <div 
          class="group relative w-full aspect-square rounded-xl overflow-hidden shadow-lg max-w-[280px] sm:max-w-none mx-auto"
          on:click={() => project.link && window.open(project.link, '_blank', 'noopener,noreferrer')}
          role={project.link ? 'link' : 'presentation'}
          style={project.link ? 'cursor: pointer' : ''}
        >
          <img
            src={project.image}
            alt={project.title}
            class="w-full h-full object-cover transition-all duration-500 group-hover:scale-110 group-hover:rotate-2"
          />
          <div class="absolute inset-0 bg-gradient-to-t from-black via-gray-900/90 to-transparent opacity-0 group-hover:opacity-100 transition-all duration-300 pointer-events-none">
            <div class="absolute bottom-0 left-0 right-0 p-3 sm:p-6">
              <h3 class="text-base sm:text-xl font-semibold text-gray-50 mb-1 sm:mb-2">{project.title}</h3>
              <p class="text-xs sm:text-sm text-gray-200/90 mb-2 sm:mb-4">{project.description}</p>
              <div class="flex flex-wrap gap-1 sm:gap-2">
                {#each project.platforms as platform}
                  <span class="inline-block px-2 sm:px-3 py-0.5 sm:py-1 bg-gray-200/20 backdrop-blur-sm rounded-full text-[10px] sm:text-xs font-medium text-gray-100">
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