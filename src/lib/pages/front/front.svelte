<script setup>
  import {
    faGithub,
    faDiscord,
    faLinkedin,
    faTwitter,
    faYoutube,
    faMastodon,
  } from "@fortawesome/free-brands-svg-icons";

  import Icon from "$lib/components/icon.svelte";
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
      <div class="flex justify-center mt-3">
        <Icon
          href="https://github.com/dnorhoj"
          icon={faGithub}
          target="_blank"
        />
        <Icon
          href="javascript:alert('Add me on discord: dnorhoj#1337')"
          icon={faDiscord}
        />
        <Icon
          href="https://www.linkedin.com/in/daniel-norhoj/"
          icon={faLinkedin}
          target="_blank"
        />
        <Icon
          href="https://fosstodon.org/@dnorhoj"
          icon={faMastodon}
          target="_blank"
        />
        <Icon
          href="https://twitter.com/dnorhoj"
          icon={faTwitter}
          target="_blank"
        />
        <Icon
          href="https://youtu.be/dQw4w9WgXcQ"
          icon={faYoutube}
          target="_blank"
        />
      </div>
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
