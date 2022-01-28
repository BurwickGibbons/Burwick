<script>
	import Logo from './Logo.svelte'
	import Hamburger from './Hamburger.svelte'
	import Menu from './Menu.svelte'

	
	
	export let sidebar = false
</script>

<header class="z-20 flex justify-between bg-zinc-200 items-center shadow-lg">
	<nav class="flex z-20">
			<Hamburger bind:open={sidebar}/>
			
	</nav>
	<Menu/>
	
</header>
