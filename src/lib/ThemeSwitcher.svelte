<script lang="ts">
	import { browser } from '$app/environment';
	import 'iconify-icon';
	let theme = 'light';
	if (browser) {
		const browserPreference = window.matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light';
		if (localStorage.getItem('theme') === null) 
			localStorage.setItem('theme', browserPreference);
		theme = localStorage.getItem('theme') ?? 'light';
	}

	$: {
		if (browser) {
			console.log('reactive update');
			if (theme === 'dark') {
				document.querySelector('html')?.classList.add('dark');
				localStorage.setItem('theme', 'dark');
			} else {
				document.querySelector('html')?.classList.remove('dark');
				localStorage.setItem('theme', 'light');
			}
		}
	}



	const toggleTheme = () => (theme = theme === 'dark' ? 'light' : 'dark');
</script>
<button on:click={toggleTheme} class="fixed bottom-3 left-3 h-fit w-fit bg-gray-700 dark:bg-gray-300 p-3 rounded-[100%] border-2 border-yellow-600 text-yellow-600 flex items-center justify-center">
{#if theme === 'dark'}
<iconify-icon icon="ph:sun-fill"/>
{:else}
<iconify-icon icon="ph:moon-fill"/>
{/if}
</button>
