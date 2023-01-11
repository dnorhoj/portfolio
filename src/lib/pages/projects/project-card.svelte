<script lang="ts">
  import Fa from "svelte-fa";
  import type { IconDefinition } from "@fortawesome/fontawesome-common-types";

  export let title: string, icon: IconDefinition, description: string, lang: string;
</script>

<template>
  <div class="container">
    <div>
      <div class="title">
        <Fa class="inline" icon={icon} />
        <h1 class="ml-1 inline text-base xl:text-lg font-bold">
          <span>{title}</span>
        </h1>
      </div>
      <div class="p-2">
        <span class="text-sm xl:text-base font-normal">{description}</span>
      </div>
    </div>
    <div class="footer">
      <div class="footer-sep">
        <span class="text-xs xl:text-sm">{lang}</span>
        <div class="links">
          <slot />
        </div>
      </div>
    </div>
  </div>
</template>

<style>
  .container {
    @apply bg-white w-64 xl:w-72 rounded-xl drop-shadow-xl flex flex-col justify-between overflow-hidden;
  }

  .title {
    @apply p-2 bg-neutral-800 rounded-b-xl text-white drop-shadow-lg;
  }

  .footer {
    @apply p-2 bg-neutral-800 rounded-t-xl text-white drop-shadow-lg;
  }

  .footer-sep {
    @apply flex justify-between items-center;
  }

  .links {
    @apply flex;
  }

  .links > :global(a) {
    @apply p-1 text-lg xl:text-xl transition-all rounded-lg bg-transparent hover:bg-neutral-700;
  }
</style>
