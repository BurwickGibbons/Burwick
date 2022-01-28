<script>

	export let open = false
	let padding = 5
</script>



<aside class="absolute w-full h-full bg-zinc-200 border-r-2 shadow-lg z-20 rounded-tr-lg " class:open>
<aside class="y=20 x=30 absolute w-full h-20 bg-slate-700 shadow-lg z-20 rounded-br-full" class:open></aside>
	<nav class="p-12 py-20">

		<a class="block py-2" href="/" on:click={()=>open=false}>Home</a>
		<a class="block py-2" href="/about" on:click={()=>open=false}>About</a>
		<a class="block py-2" href="/blender" on:click={()=>open=false}>Blender</a>
		<a class="block py-2" href="/piano" on:click={()=>open=false}>Piano</a>
		<a class="block py-2" href="/cv" on:click={()=>open=false}>CV</a>
		<a class="block py-2" href="/contact" on:click={()=>open=false}>Contact</a>

	</nav>

</aside>



<style lang="postcss">

	a {
		@apply text-2xl;
		@apply text-slate-700;
		transition: font .5s;	
	}

	a:hover {
		@apply font-bold;
		@apply text-slate-900;
		@apply text-3xl;
	}


	aside {
		left: -100%;
		transition: left .5s ease-in-out;
	}

	
	
	.open {
		left: 0
	}



</style>