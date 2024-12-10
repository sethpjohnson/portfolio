<script lang="ts">
  import { experiences } from '$lib/data/experiences';
</script>

<section class="py-16 bg-gray-50" id="experience">
  <div class="container mx-auto px-6">
    <h2 class="text-3xl font-bold mb-8 text-gray-900">Experience</h2>
    <div class="space-y-8">
      {#each experiences as exp}
        <div class="bg-white p-6 rounded-lg shadow-lg border border-gray-100">
          <h3 class="text-xl font-semibold text-gray-900">{exp.title}</h3>
          <p class="text-purple-700 mb-2">{exp.company}</p>
          <p class="text-gray-600 text-sm mb-4">{exp.period}</p>
          <ul class="space-y-2">
            {#each exp.description as item}
              <li class="flex text-gray-700">
                <span class="mr-2 flex-shrink-0">•</span>
                <span>{item}</span>
              </li>
            {/each}
          </ul>
        </div>
      {/each}
    </div>
  </div>
</section>