<script>
	import { fly } from 'svelte/transition';
	let visible = true;

	export let open = false;
	const links = [
		{ title: 'Home', href: '/' },
		{ title: 'About', href: '/about' },
		{ title: 'Blender', href: '/blender' },
		{ title: 'Piano', href: '/piano' },
		{ title: 'CV', href: '/cv' },
		{ title: 'Contact', href: '/contact' },
		{ title: 'Test', href: '/test' }

	];
</script>

<aside
	class="absolute w-full h-full bg-zinc-200 border-r-2 shadow-lg z-20 rounded-tr-lg "
	class:open
>
	<div class="w-[110%] h-20 bg-slate-700 shadow-lg z-20 rounded-br-full" class:open />
	{#key open}
		<nav class="p-5 px-20">
			{#each links as { href, title }, index}
				<a
					in:fly={{ x: -200, duration: 200, delay: 200 + index * 200 }}
					class="py-2 block"
					{href}
					on:click={() => (open = false)}>{title}</a
				>
			{/each}
		</nav>
	{/key}
</aside>

<style lang="postcss">
	a {
		@apply text-2xl;
		@apply text-slate-700;
		transition: font 0.5s;
	}

	a:hover {
		@apply font-bold;
		@apply text-slate-900;
		@apply text-3xl;
	}

	aside {
		left: -120%;
		transition: left 0.5s ease-in-out;
	}
	div {
		left: -100%;
		transition: left 0.5s ease-in;
	}

	.open {
		left: 0;
	}
</style>
