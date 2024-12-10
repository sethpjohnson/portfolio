<script lang="ts">
  import { skills } from '$lib/data/skills';
</script>

<section class="py-16 bg-white" id="skills">
  <div class="container mx-auto px-6">
    <h2 class="text-3xl font-bold mb-8 text-gray-900">Skills</h2>
    <div class="grid md:grid-cols-3 gap-8">
      {#each skills as skillSet}
        <div class="bg-gradient-to-br from-purple-100 to-blue-100 p-6 rounded-lg shadow-lg border border-purple-200">
          <h3 class="text-xl font-semibold mb-4 text-gray-900">{skillSet.category}</h3>
          <ul class="space-y-2">
            {#each skillSet.items as skill}
              <li class="text-gray-700 flex items-center">
                <span class="w-2 h-2 bg-purple-600 rounded-full mr-2"></span>
                {skill}
              </li>
            {/each}
          </ul>
        </div>
      {/each}
    </div>
  </div>
</section>