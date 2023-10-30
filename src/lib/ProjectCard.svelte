<script lang="ts">
import 'iconify-icon';

export let title: string;
export let github: string;
export let deploy: string | false = false;
export let thumbnail: string;
export let stack: string[];
const stackString = stack.join(', ');
</script>
<!--
// v0 by Vercel.
// https://v0.dev/t/LQbuXYzXPwV
-->

<div
  class="border bg-card text-card-foreground max-w-md mx-auto shadow-lg rounded-lg overflow-hidden m-5 flex justify-between flex-col"
  data-v0-t="card"
>
  <img
    src={ thumbnail }
    height="200"
    width="400"
    alt="Project Thumbnail"
    class="w-full h-64 object-cover aspect-[400/200] object-center rounded-t"
  />
  <div class="p-6 px-6 py-4">
    <h3 class="tracking-tight text-xl font-semibold">{ title }</h3>
    <p class="text-base text-gray-600 dark:text-white mt-2">
	<slot/>
    </p>
    <div class="flex items-center mt-4 text-gray-700 dark:text-white">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
        class=" h-5 w-5"
      >
        <polyline points="16 18 22 12 16 6"></polyline>
        <polyline points="8 6 2 12 8 18"></polyline>
      </svg>
      <h3 class="px-2 text-sm">{ stackString }</h3>
    </div>
  </div>
  <div class="p-6 flex items-center justify-between px-6 py-3 bg-gray-100 dark:bg-gray-800">
    <a target="_blank" href={github} class="inline-flex gap-2 items-center justify-center rounded-md font-medium ring-offset-background transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 disabled:pointer-events-none disabled:opacity-50 border border-input bg-background hover:bg-accent hover:text-accent-foreground h-10 px-4 py-2 text-sm">
	  <iconify-icon icon="mdi:github"/>
	  Github
    </a>
	{#if deploy !== false}
    <a target="_blank" href={deploy} class="inline-flex gap-2 items-center justify-center rounded-md font-medium ring-offset-background transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 disabled:pointer-events-none disabled:opacity-50 border border-input bg-background hover:bg-accent hover:text-accent-foreground h-10 px-4 py-2 text-sm">
	  <iconify-icon icon="mdi:link"/>
	  Production
    </a>
	{/if}
  </div>
</div>
