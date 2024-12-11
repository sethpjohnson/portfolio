<script>
  import { education } from "$lib/data/education";
  import { base } from "$app/paths";
</script>

<section class="py-16 bg-gray-50" id="education">
  <div class="container mx-auto px-6 flex flex-col gap-2">
    <h2 class="text-3xl font-bold mb-8 text-gray-900">Education</h2>
    <div class="flex flex-col gap-2">
      {#each education as item}
        <div class="flex flex-row gap-4 items-center">
          <div class="flex-shrink-0">
            <img src={`${base}${item.image}`} alt={item.title} class="w-16 h-16 flex-shrink-0" />
          </div>
          <div>
            <p>
              <span class="text-xl font-semibold text-gray-900">{item.title}</span> |
              <span class="text-gray-700">{item.date}</span> | 
              <span class="text-purple-700">{item.items.join(", ")}</span>
            </p>
          </div>
        </div>
      {/each}
    </div>
  </div>
  
</section>