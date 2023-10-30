<script lang="ts">
	import Nav from "$lib/Nav.svelte";
	import ThemeSwitcher from "$lib/ThemeSwitcher.svelte";
	import '../global.css';
</script>

<ThemeSwitcher />
<main class="bg-gray-100 dark:bg-gray-900 dark:text-white w-full lg:w-1/2 my-0 mx-auto p-4">
<slot />
</main>
<Nav />
