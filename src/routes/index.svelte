<script>
	import SocialMediaTags from '$lib/Components/SocialMediaTags.svelte';
	import BackgroundPano from '$lib/Components/BackgroundPano.svelte';
	import HomeDesc from '$lib/Components/HomeDesc.svelte';



</script>

<title>Home</title>

<div 
class="relative"
>
	<BackgroundPano />
</div>


<div
	class="container relative mx-auto justify-center"
	>
	<div
		class="card"
		>
		<h1>Heading 1</h1>
		<p>texteuifhqwuifhasoigjwqeoighieqw ghoqwignoiwqg9iqnwg9 haignaoiniunu</p>
	</div>
	<div
		class="card"
		>
		<h2>Heading 2</h2>
		<p>texteuifhqwui fhasoigjwqeoighieqw ghoqwignoiwqg9iqnwg9 haignaoiniunu</p>
	</div>
</div>

<footer class="footer left-0 bottom-0 right-0 scale-50 sm:scale-100">
	<SocialMediaTags />
</footer>


<style lang="postcss">

	.container{
		@apply bg-slate-300;
		width: auto;
		height: auto;
		border-radius: 20px;
		display: flex;
		flex-direction: raw;
		gap: 40%;
		padding: 30px;
		
	}
	.card{
		@apply bg-slate-100;
		width: 30%;
		max-width: 1000px;
		height: auto;
		border-radius: 10px;
		padding: 5px 15px;


	}
	@media screen and (max-width: 600px) {
		.container{
			flex-direction: column;
		}

		.card{
			width: auto;
			height: auto;
			padding: 5px 15px;
		}
	}
	@media screen and (max-width: 1000px) {
		.footer{
			@apply absolute;
		}
	}

</style>