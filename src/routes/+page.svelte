<script lang="ts">
	import Card from '$lib/Card.svelte';
	import ProjectCard from '$lib/ProjectCard.svelte';
import 'iconify-icon';
</script>

<section id="about" class="flex flex-col min-h-screen md:min-h-fit sm:justify-center justify-between gap-5 pb-10">
	<div class="welcome flex gap-4 text-8xl flex-col md:flex-row">
		<img class="md:h-60 md:w-60 h-14 w-14 object-cover object-center rounded-[100%] border-2 border-black dark:border-white md:block" src="https://media.discordapp.net/attachments/1153926751479668797/1168214402596618260/20230813_132143.jpg" alt="Isaac" />
		<span class="font-normal">
			<h1>Hi 👋,</h1>
			<h1>I'm <span class="font-bold">Isaac</span></h1>
		</span>
	</div>
	<p id="description" class="text-2xl">
	A Software Engineering BEng student at Sheffield Hallam University looking for a placement position.
	For the past 2 years I have been focusing on Web Technologies however, I have experience in many other areas of Software Engineering. 
	Thanks for taking the time to checkout what im up to!
	</p>
	<a class="block md:hidden underline hover:brightness-75" href="#projects">Learn More</a>
</section>

<h2 class="text-4xl pt-4" id="projects">Projects</h2>
<section id="projects-content" class="flex flex-wrap mb-8">
	<ProjectCard 
	thumbnail="https://cdn.discordapp.com/attachments/659103295771770880/1168202896781885550/image.png" 
	title="Nuxt 3 Blog" 
	github="https://github.com/isaac238/nuxtBlog" 
	deploy="https://blog.isaac238.dev" 
	stack={["Nuxt3", "Vue3", "TypeScript", "Supabase", "Vercel"]}>
	This is a blog website I built using Nuxt 3 with Typescript and Tailwind CSS for the front-end,
	Supabase for database, authentication and storing md files as articles, and Vercel for deployment.
	</ProjectCard>

	<ProjectCard 
	thumbnail="https://cdn.discordapp.com/attachments/659103295771770880/1168222254186897479/image.png" 
	title="Codle" 
	github="https://github.com/isaac238/codle" 
	deploy="https://codle.isaac238.dev" 
	stack={["NextJS", "React", "TypeScript", "Vercel KV (Redux)", "Vercel Crons", "Vercel"]}>
	This is a wordle based website I built using NextJS 13 with Typescript and Tailwind CSS for the front-end.
	As well as Vercels KV database for storing programming related answers, Vercels Cron-job feature for scheduling a change each day, and Vercel for deployment.
	</ProjectCard>
</section>

<h2 class="text-4xl pt-4" id="technologies">Technologies</h2>
<section id="technologies-content" class="flex flex-wrap mb-8 gap-1">
	<Card icon="logos:typescript-icon" title="Typescript"/>
	<Card icon="logos:javascript" title="Javascript"/>
	<Card icon="logos:html-5" title="HTML"/>
	<Card icon="logos:css-3" title="CSS"/>
	<Card icon="logos:c-sharp" title="C#"/>
	<Card icon="logos:python" title="Python"/>
	<Card icon="logos:java" title="Java"/>
	<Card icon="logos:mysql" title="MySQL"/>
	<Card icon="logos:sqlite" title="SQLite"/>
	<Card icon="devicon-plain:jquery-wordmark" title="JQuery"/>
	<Card icon="logos:svelte-icon" title="Svelte"/>
	<Card icon="logos:nuxt-icon" title="Nuxt 3"/>
	<Card icon="logos:vue" title="Vue 3"/>
	<Card icon="logos:nextjs-icon" title="NextJS 13"/>
	<Card icon="logos:react" title="React"/>
	<Card icon="logos:tailwindcss-icon" title="Tailwind"/>
	<Card icon="logos:supabase-icon" title="Supabase"/>
	<Card icon="simple-icons:pocketbase" title="Pocketbase"/>
	<Card icon="logos:vercel-icon" title="Vercel"/>
</section>