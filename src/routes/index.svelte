<script>
	import SocialMediaTags from '$lib/Components/SocialMediaTags.svelte';
	import BackgroundPano from '$lib/Components/BackgroundPano.svelte';
	import HomeDesc from '$lib/Components/HomeDesc.svelte';



</script>

<title>Reuben's Website Home</title>

<div 
class="relative"
>
	<BackgroundPano />
</div>


<HomeDesc/>

<footer class="footer left-0 bottom-0 right-0 scale-50 sm:scale-100">
	<SocialMediaTags />
</footer>


<style lang="postcss">

	@media screen and (max-width: 800px) {
		.footer{
			@apply absolute;
		}
	}

</style>