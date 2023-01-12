<script lang="ts">
  import SocialIcons from "$lib/components/social-icons.svelte";
  import { faClipboard } from "@fortawesome/free-regular-svg-icons";
  import Fa from "svelte-fa";

  let copied = false;

  async function copy() {
    await navigator.clipboard.writeText("daniel@dnorhoj.me");
    copied = !copied;
    setTimeout(() => {
      copied = false;
    }, 1200);
  }
</script>

<template>
  <div class="contact" id="contact">
    <h1 class="title">Contact</h1>
    <div class="card">
      <div class="content">
        <h1 class="p-5 text-center text-white font-semibold text-2xl underline">
          Social Links
        </h1>
        <SocialIcons class="flex justify-center p-5" />
      </div>
      <hr class="border-2 border-black border-opacity-50" />
      <div class="content">
        <h1 class="p-5 text-center text-white font-semibold text-2xl underline">
          Email
        </h1>
        <div class="flex justify-center p-5">
          <div class="bg-white rounded-lg shadow-xl flex items-center">
            <span class="pl-2 pr-1">daniel@dnorhoj.me</span>
            <div class="relative">
              <div class="flex flex-col">
                <button
                  on:click={copy}
                  aria-label="Copy email address"
                  class="p-3 rounded-lg transition-all hover:bg-neutral-300"
                >
                  <Fa icon={faClipboard} />
                </button>
                {#if copied}
                  <div
                    class="bg-green-500 text-white text-center rounded-tl-none rounded-xl p-2 absolute top-10"
                  >
                    Copied!
                  </div>
                {/if}
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div
      class="absolute bottom-0 bg-neutral-800 w-full p-2 text-white flex justify-between rounded-t-lg"
    >
      <span>© Daniel Norhøj - 2022</span>
      <span>
        Check out the code on
        <a
          class="underline"
          href="https://github.com/dnorhoj/dnorhoj.me"
          target="_blank"
          rel="noreferrer"
        >
          GitHub</a
        >!
      </span>
    </div>
  </div>
</template>

<style>
  .card {
    @apply bg-opacity-60 bg-black rounded-2xl border-black border-opacity-50 border-4 mt-5 flex flex-col drop-shadow-xl;
  }

  .content {
    @apply flex flex-col;
  }

  .contact {
    @apply relative flex justify-center items-center flex-col snap-center h-screen;
  }

  .title {
    @apply inline font-bold text-white drop-shadow-lg text-center text-3xl md:text-5xl;
  }
</style>
