<script lang="ts">
  import SkillCard from "./skill-card.svelte";

  import {
    faLock,
    faCode,
    faDatabase,
  } from "@fortawesome/free-solid-svg-icons";
  import {
    faPython,
    faJs,
    faHtml5,
    faGitAlt,
    faLinux,
    faDocker,
  } from "@fortawesome/free-brands-svg-icons";
</script>

<template>
  <div class="skills" id="skills">
    <h1 class="title">Skills</h1>
    <div class="skill-container">
      <SkillCard icon={faLock} title="Cybersecurity" />
      <SkillCard icon={faCode} title="Software development" />
      <SkillCard icon={faDocker} title="Docker" />
      <SkillCard icon={faPython} title="Python" />
      <SkillCard icon={faJs} title="JavaScript" />
      <SkillCard icon={faHtml5} title="HTML/CSS" />
      <SkillCard icon={faGitAlt} title="Git" />
      <SkillCard icon={faLinux} title="Linux" />
      <SkillCard icon={faDatabase} title="Database" />
    </div>
  </div>
</template>

<style>
  .skills {
    @apply relative flex justify-center items-center
      flex-col lg:flex-row snap-center h-screen;
  }

  .title {
    @apply inline font-bold text-white drop-shadow-lg text-center text-3xl md:text-5xl;
  }

  .skill-container {
    @apply grid md:grid-cols-2 lg:grid-cols-3 justify-center border-white border-t-2 mt-4 p-3
      max-h-[75vh] overflow-auto lg:border-t-0 lg:border-l-2 lg:mt-0 lg:ml-4;
  }

  .skill-container > :global(*) {
    @apply m-2;
  }
</style>
