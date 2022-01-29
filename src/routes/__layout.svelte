<script>
	import '../app.css';
	import SocialMediaTags from '$lib/Components/SocialMediaTags.svelte';
	import Navbar from '$lib/Components/Navbar.svelte';
	import Sidebar from '$lib/Components/Sidebar.svelte';

	let open = false;
</script>

<Sidebar bind:open />
<Navbar bind:sidebar={open} />

<!-- <svelte:head>
	  <link href="https://unpkg.com/tailwindcss@^1.0/dist/tailwind.min.css" rel="stylesheet"/>
  </svelte:head> -->

<slot />


<footer class="absolute left-0 bottom-0 right-0 scale-50 sm:scale-100">
	<SocialMediaTags />
</footer>

<style lang="postcss">
	:global(body) {
    @apply h-full;
		/* background-color:rgb(243, 243, 243); */
		@apply bg-zinc-100;
		padding: 0;
		@apply font-informal;
	}
	col {
		@apply bg-red-600;
	}
</style>
