<script lang="ts">
  import ProjectCard from "./project-card.svelte";

  import { faGlobe } from "@fortawesome/free-solid-svg-icons";
  import { faGithub, faPython, faChrome } from "@fortawesome/free-brands-svg-icons";

  import Fa from "svelte-fa";
</script>

<template>
  <div class="projects" id="projects">
    <h1 class="title">Projects</h1>
    <div class="project-container">
      <ProjectCard
        title="AntiRickRoll"
        icon={faChrome}
        description="Browser extension that blocks Rickrolls!"
        lang="JS, HTML"
      >
        <a
          href="https://antirickroll.com/"
          aria-label="AntiRickRoll website"
          target="_blank"
          rel="noreferrer"
        >
          <Fa icon={faGlobe} fw />
        </a>
        <a
          href="https://github.com/dnorhoj/AntiRickRoll"
          aria-label="AntiRickRoll GitHub Repository"
          target="_blank"
          rel="noreferrer"
        >
          <Fa icon={faGithub} fw />
        </a>
      </ProjectCard>
      <ProjectCard
        title="Lectio.py"
        icon={faPython}
        description="Python library which interfaces the Lectio website through HTTP requests."
        lang="Python"
      >
        <a
          href="https://pypi.org/project/lectio.py/"
          aria-label="Lectio.py website"
          target="_blank"
          rel="noreferrer"
        >
          <Fa icon={faGlobe} fw />
        </a>
        <a
          href="https://github.com/dnorhoj/lectio.py"
          aria-label="Lectio.py GitHub Repository"
          target="_blank"
          rel="noreferrer"
        >
          <Fa icon={faGithub} fw />
        </a>
      </ProjectCard>
      <ProjectCard
        title="Unnamed Discord Bot"
        icon={faPython}
        description="Unnamed general purpose discord bot."
        lang="Python"
      >
        <a
          href="https://github.com/dnorhoj/unnameddiscordbot"
          aria-label="Unnamed Discord Bot GitHub Repository"
          target="_blank"
          rel="noreferrer"
        >
          <Fa icon={faGithub} fw />
        </a>
      </ProjectCard>
    </div>
  </div>
</template>

<style>
  .projects {
    @apply relative flex justify-center items-center flex-col snap-center h-screen;
  }

  .title {
    @apply inline font-bold text-white drop-shadow-lg text-center text-3xl md:text-5xl;
  }

  .project-container {
    @apply grid md:grid-cols-2 lg:grid-cols-3 justify-center border-white border-t-2 mt-4 p-3 max-h-[75vh] overflow-auto;
  }

  .project-container > :global(*) {
    @apply m-2;
  }
</style>
