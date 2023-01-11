<script lang="ts">
  import Fa from "svelte-fa";
  import { faBars, faBarsStaggered } from "@fortawesome/free-solid-svg-icons";

  export let title: string, pages: string[][];

  let hidden = true;

  const toggleHidden = () => {
    hidden = !hidden;
  };
</script>

<template>
  {#if hidden}
    <button on:click={toggleHidden} class="nav-extender">
      <Fa icon={faBars} />
    </button>
  {:else}
    <div class="nav">
      <div class="nav-title">
        <button class="close" on:click={toggleHidden}>
          <Fa icon={faBarsStaggered} />
        </button>
        <span>{title}</span>
        <div class="w-10" />
      </div>
      <hr />
        <button class="nav-content" on:click={toggleHidden}>
          {#each pages as page}
            <a class="nav-item" href={page[1]}>{page[0]}</a>
          {/each}
        </button>
    </div>
  {/if}
</template>

<style>
  .nav-extender {
    @apply fixed m-5 w-10 h-10 bg-white rounded-lg z-10 flex justify-center items-center cursor-pointer hover:bg-neutral-300 drop-shadow-xl;
  }

  .nav {
    @apply fixed m-5 z-20 drop-shadow-xl bg-white rounded-lg overflow-hidden w-[calc(100%-2.5rem)] md:w-auto;
  }

  .nav-title {
    @apply flex justify-between;
  }

  .nav-title > * {
    @apply p-2 font-bold;
  }

  .nav-title > .close {
    @apply hover:bg-neutral-300 rounded-lg w-10 h-10 cursor-pointer flex justify-center items-center;
  }

  .nav-content {
    @apply flex flex-col items-center flex-grow w-full;
  }

  .nav-item {
    @apply p-1 hover:bg-neutral-800 hover:text-white w-full text-center;
  }
</style>
