<script lang="ts">
  import SocialIcons from "$lib/components/social-icons.svelte";
</script>

<template>
  <div class="relative flex justify-center snap-center h-screen" id="front">
    <div class="flex flex-col justify-center w-full">
      <h1 class="text-4xl lg:text-5xl titletext">Daniel Norhøj</h1>
      <h2 class="text-xl lg:text-2xl my-3 titletext">
        Student | Developer | Ethical Hacking
      </h2>
      <hr
        class="border-2 mt-3 drop-shadow-lg 2xl:w-1/3 xl:w-1/2 lg:w-1/2 w-11/12 rounded-full self-center"
      />
      <SocialIcons class="flex justify-center mt-3" />
    </div>
    <div class="absolute bottom-3 animate-bounce">
      <a class="text-white text-xl font-bold" href="#projects">
        Scroll for more!
      </a>
    </div>
  </div>
</template>

<style>
  .titletext {
    @apply inline font-bold text-white drop-shadow-lg text-center;
  }
</style>
