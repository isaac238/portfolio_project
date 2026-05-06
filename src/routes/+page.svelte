<script lang="ts">
	import Card from '$lib/Card.svelte';
	import ProjectCard from '$lib/ProjectCard.svelte';
	import 'iconify-icon';
	import Me from '$lib/Me.jpg';
	import NuxtBlog from '$lib/NuxtBlog.png';
	import Codle from '$lib/Codle.png';
	import RandomDroid from '$lib/DroidDB.png';
	import Neovim from '$lib/Neovim.png';
</script>

<section
	id="about"
	class="flex flex-col min-h-screen md:min-h-fit sm:justify-center justify-between gap-5 pb-10"
>
	<div class="welcome flex gap-4 text-8xl flex-col md:flex-row">
		<img class="md:h-60 md:w-60 h-14 w-14 object-cover object-center rounded-[100%] border-2 border-black dark:border-white md:block" src={Me} alt="Isaac" />

		<div class="flex-grow-0 flex-shrink basis-0">
			<h1 class="font-bold">Isaac Sutherland</h1>
			<h2 class="font-thin brightness-75 text-2xl">Graduate Software Engineer @ Raytheon</h2>

			<ul class="flex gap-4 mt-2 border-2 dark:border-gray-200 border-black rounded-md p-1 w-fit">
				<li>
					<a class="flex justify-center align-center hover:brightness-50" href="https://www.linkedin.com/in/isaac-sutherland-007b42239/">
						<iconify-icon icon="mdi:linkedin" width="2rem" height="2rem"></iconify-icon>
					</a>
				</li>

				<li>
					<a class="flex justify-center align-center hover:brightness-75" href="https://www.github.com/isaac238">
						<iconify-icon icon="mdi:github" width="2rem" height="2rem"></iconify-icon>
					</a>
				</li>
			</ul>
		</div>
	</div>
	<p id="description" class="text-2xl">
	</p>
</section>

<h2 class="text-4xl pt-4" id="projects">Projects</h2>
<hr class="mt-2 mb-2" />
<section id="projects-content" class="flex flex-wrap mb-8">
	<ProjectCard
		thumbnail={NuxtBlog}
		title="Nuxt 3 Blog"
		github="https://github.com/isaac238/nuxtBlog"
		deploy="https://blog.isaac238.dev"
		stack={['Nuxt3', 'Vue3', 'TypeScript', 'Supabase', 'Vercel', 'Tailwind']}
	>
		This is a blog website I built using Nuxt 3 with Typescript and Tailwind CSS for the front-end,
		Supabase for database, authentication and storing md files as articles, and Vercel for
		deployment.
	</ProjectCard>

	<ProjectCard
		thumbnail={Codle}
		title="Codle"
		github="https://github.com/isaac238/codle"
		deploy="https://codle.isaac238.dev"
		stack={[
			'NextJS',
			'React',
			'TypeScript',
			'Tailwind',
			'Vercel KV (Redux)',
			'Vercel Crons',
			'Vercel'
		]}
	>
		This is a wordle based website I built using NextJS 13 with Typescript and Tailwind CSS for the
		front-end. As well as Vercels KV database for storing programming related answers, Vercels
		Cron-job feature for scheduling a change each day, and Vercel for deployment.
	</ProjectCard>

	<ProjectCard
		thumbnail={RandomDroid}
		title="Random Droid"
		github="https://github.com/isaac238/RandomDroid"
		deploy="https://droids.isaac238.dev"
		stack={['SvelteKit', 'Tailwind', 'TypeScript', 'Vercel', 'Python']}
	>
		This is a website built using SvelteKit, Tailwind, and TypeScript for the front-end. That makes
		use of python to webscrape the Star Wars Wiki. Into an API that is then used to display random
		droids on the website.
	</ProjectCard>

	<ProjectCard
		thumbnail={Neovim}
		title="Terminal_Run.nvim"
		github="https://github.com/isaac238/Terminal_Run.nvim"
		stack={['Lua']}
	>
		This is a plugin for neovim that allows you to set a command for each working directory and then
		run it with :Run to open it in a new terminal buffer.
	</ProjectCard>
</section>

<h2 class="text-4xl pt-4" id="technologies">Technologies</h2>
<hr class="mt-2 mb-2" />
<section id="technologies-content" class="flex flex-wrap justify-start mb-8 gap-3">
	<Card icon="logos:typescript-icon" title="Typescript" />
	<Card icon="logos:javascript" title="Javascript" />
	<Card icon="logos:html-5" title="HTML" />
	<Card icon="logos:css-3" title="CSS" />
	<Card icon="logos:nodejs-icon" title="Node" />
	<Card icon="logos:php" title="PHP" />
	<Card icon="logos:c-sharp" title="C#" />
	<Card icon="logos:python" title="Python" />
	<Card icon="logos:java" title="Java" />
	<Card icon="logos:lua" title="Lua" />
	<Card icon="logos:sqlite" title="SQLite" />
	<Card icon="devicon-plain:jquery-wordmark" title="JQuery" />
	<Card icon="logos:svelte-icon" title="Svelte" />
	<Card icon="logos:nuxt-icon" title="Nuxt 3" />
	<Card icon="logos:vue" title="Vue 3" />
	<Card icon="logos:tailwindcss-icon" title="Tailwind" />
	<Card icon="logos:supabase-icon" title="Supabase" />
	<Card icon="simple-icons:pocketbase" title="Pocketbase" />
</section>
