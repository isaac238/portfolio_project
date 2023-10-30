<script lang="ts">
	import Nav from "$lib/Nav.svelte";
	import ThemeSwitcher from "$lib/ThemeSwitcher.svelte";
	import '../global.css';
</script>

<svelte:head>
<title>Portfolio | Isaac</title>
<meta name="description" content="Isaac's portfolio website" />
</svelte:head>

<ThemeSwitcher />
<main class="bg-gray-100 dark:bg-gray-900 dark:text-white w-full lg:w-1/2 my-0 mx-auto p-4">
<slot />
</main>
<Nav />
