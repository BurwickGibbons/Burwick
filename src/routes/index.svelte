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
class="relative"
>


	<HomeDesc />
</div>

<footer class="absolute left-0 bottom-0 right-0 scale-50 sm:scale-100">
	<SocialMediaTags />
</footer>

