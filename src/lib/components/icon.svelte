<script lang="ts">
  import type { IconDefinition } from "@fortawesome/fontawesome-common-types";
  import Fa from "svelte-fa";

  export let icon: IconDefinition, href: string, target: string = "self";
</script>

<template>
  <a class="icon" {href} {target}>
    <Fa icon={icon} class="text-neutral-700 text-4xl" fw />
  </a>
</template>

<style>
  .icon {
    @apply py-3 px-2 mx-1 bg-white rounded-xl drop-shadow-lg hover:-translate-y-1 transition-all hover:drop-shadow-xl cursor-pointer;
  }
</style>
