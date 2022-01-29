<script>
	import SocialMediaTags from '$lib/Components/SocialMediaTags.svelte';
	import BackgroundPano from '$lib/Components/BackgroundPano.svelte';

	let herePeter = false;

	const handleMouseenter = () => herePeter = true;
	const handleMouseleave = () => herePeter = false;
</script>

<title>Home</title>

<div class="relative">
	<BackgroundPano />
</div>

<svelte:body
on:mouseenter={handleMouseenter}
on:mouseleave={handleMouseleave}
/>

<!-- creative commons BY-NC http://www.pngall.com/kitten-png/download/7247 -->
<button on:click={handleMouseleave}>
<img class="w-1/6 h/1/6"
class:curious={herePeter}
alt="Kitten wants to know what's going on"
src="/Peter.png"
>
</button>


<style lang="postcss">
	img {
		position: absolute;
		left: 0;
		@apply bottom-0;
		transform: translate(-160%, 0) rotate(80deg);
		transform-origin: 100% 100%;
		transition: transform 1s;
	}
	
	.curious {
		transform: translate(-110%, 0) rotate(90deg);
		transition-delay: 50ms;

	}
	
	img:hover.curious {
		transform: translate(-120%, 0) rotate(80deg);
		transition: transform 1s;
	}
	</style>
