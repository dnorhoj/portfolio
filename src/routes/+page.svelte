<script lang="ts">
  import Navigation from "$lib/components/navigation.svelte";

  import Front from "$lib/pages/front/front.svelte";
  import Projects from "$lib/pages/projects/projects.svelte";
  import Skills from "$lib/pages/skills/skills.svelte";
  import Contact from "$lib/pages/contact/contact.svelte";
</script>

<template>
  <!-- TODO: navbar / CTRL K ting -->
  <Navigation
    title="Daniel Norhøj"
    pages={[
      ["Frontpage", "#front"],
      ["Projects", "#projects"],
      ["Skills", "#skills"],
      ["Contact", "#contact"],
    ]}
  />
  <!-- svelte-ignore a11y-no-noninteractive-tabindex -->
  <div tabindex="0" class="main">
    <Front />
    <Projects />
    <Skills />
    <Contact />
  </div>
</template>

<style>
  .main {
    @apply snap-y snap-mandatory overflow-y-scroll h-screen scroll-smooth bg-gradient-to-br from-red-500 to-indigo-600;
  }
</style>
