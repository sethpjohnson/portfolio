<script lang="ts">
  import Header from '$lib/components/Header.svelte';
  import About from '$lib/components/About.svelte';
  import Experience from '$lib/components/Experience.svelte';
  import Skills from '$lib/components/Skills.svelte';
  import Education from '$lib/components/Education.svelte';
  import WorkProjects from '$lib/components/WorkProjects.svelte';
  import SideProjects from '$lib/components/SideProjects.svelte';
</script>

<div class="min-h-screen bg-gray-100">
  <Header />
  <main>
    <!-- <About /> -->
    <Experience />
    <Skills />
    <WorkProjects />
    <SideProjects />
    <Education />
  </main>
  <footer class="bg-gray-950 text-white py-8">
    <div class="container mx-auto px-6 text-center">
      <p>© {new Date().getFullYear()} Seth Johnson. All rights reserved.</p>
    </div>
  </footer>
</div>