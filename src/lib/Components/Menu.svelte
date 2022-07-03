<script>
	const links = [
		{ title: 'About', href: '/about' },
		{ title: 'Contact', href: '/contact' },
		{ title: 'Home', href: '/'},
	];
</script>

<nav class="hidden md:block px-5 space-x-2">
	{#each links as { href, title }, index}
		<a {href}>{title}</a>
	{/each}
</nav>

<style lang="postcss">
	a {
		@apply text-lg;
		@apply font-bold;
		@apply text-slate-700;
		@apply uppercase;
		@apply font-title;
		transition: font 0.5s;
		border-radius: 5px;
		padding: 5px 5px;
	}
	a:hover {
		@apply text-slate-900;
		@apply underline;
	}
</style>
