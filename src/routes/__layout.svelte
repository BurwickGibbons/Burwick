<script>
  import '../app.css';
	import Navbar from '$lib/Components/Navbar.svelte'
	import Sidebar from '$lib/Components/Sidebar.svelte'
  
  
	let open = false
  </script>
  
  <Sidebar bind:open/>
  <Navbar bind:sidebar={open}/>

  
  <!-- <svelte:head>
	  <link href="https://unpkg.com/tailwindcss@^1.0/dist/tailwind.min.css" rel="stylesheet"/>
  </svelte:head> -->
  
  
  <slot></slot>


  <style lang="postcss">
	  :global(body) {
      /* background-color:rgb(243, 243, 243); */
      @apply bg-zinc-100;
		  padding: 0;
      @apply font-mono;
	  }
  </style>
  