<script>
	import { fly } from 'svelte/transition';
	let visible = true;

	export let open = false;
	const links = [
		{ title: 'Home', href: '/' },
		{ title: 'About', href: '/about' },
		{ title: 'Blender', href: '/blender' },
		{ title: 'Piano', href: '/piano' },
		{ title: 'Uniting Creativity', href: '/uniting_creativity'},
		{ title: 'CV', href: '/cv' },
		{ title: 'Contact', href: '/contact' },
		{ title: 'Test', href: '/test' }

	];
</script>

<aside
	class="absolute m-x-auto h-full border-r-4 border-b-4 sm:runded-br-none lg:rounded-br-full shadow-xl z-20 "
	class:open
>
	<div class="w-[100%] h-20 shadow-xl z-20" class:open />
	{#key open}
		<nav class="p-5 px-12">
			{#each links as { href, title }, index}
				<a
					in:fly={{ x: -200, duration: 200, delay: 300 + index * 100 }}
					class="py-3 block"
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
		@apply translate-x-0;
		@apply text-slate-700;
		transition: 500ms;
		
		
		
	}

	a:hover {
	
		@apply text-slate-900;
		@apply translate-x-2;
		
	}

	aside {
		left: -100%;
		transition: left .5s ease-in-out;
		@apply bg-slate-200;
		@apply border-slate-700;
		
	}
	div {
		left: -100%;
		transition: left .5s ease-in;
		@apply bg-slate-700;
		@apply border-slate-700;
		
	}

	.open {
		left: 0;
	}
</style>
