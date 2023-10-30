<header>
	<nav>
	<a href="">About Me</a>
	<a href="">Projects</a>
	<a href="">Skills</a>
	</nav>
</header>

<style>
header {
	display: flex;
	align-items: center;
	justify-content: space-between;
	margin-bottom: 1rem;
}

nav {
	display: flex;
	flex-direction: row;
	gap: 1rem;
	justify-content: center;
	margin-left: auto;
}

nav > a {
	text-decoration: underline 0.2rem rgba(0,0,0,0);
	font-size: 1.5rem;
}

nav > a:hover {
	text-decoration-color: black;
	transition: text-decoration-color 0.5s;
}
</style>
