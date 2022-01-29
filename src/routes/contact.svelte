<script>
	import ContactCard from '$lib/Components/ContactCard.svelte';
</script>

<title>Contact</title>

<h1 class="text-2xl font-bold text-center text-black-800 md:text-3xl">Contact</h1>

<ContactCard>
	<span slot="name">
		Reuben James Gibbons
	</span>

	<span slot="address">
		Bay View<br>
		Treligga Downs<br>
		Delabole<br>
		Cornwall<br>
		<br>
		PL33 9DQ
	</span>

	<span slot="email">
		reuben.gibbons@me.com
	</span>
</ContactCard>
