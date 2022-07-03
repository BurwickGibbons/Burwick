<script>
	let hereKitty = false;

	const handleMouseenter = () => hereKitty = true;
	const handleMouseleave = () => hereKitty = false;
</script>

<title>Reuben's Website Test</title>

<svelte:body
on:mouseenter={handleMouseenter}
on:mouseleave={handleMouseleave}
/>

<!-- creative commons BY-NC http://www.pngall.com/kitten-png/download/7247 -->
<img class="w-1/2 h/1/2"
class:curious={hereKitty}
alt="Kitten wants to know what's going on"
src="/Peter.png"
>

<style lang="postcss">
img {
	position: absolute;
	left: 0;
	@apply bottom-64;
	transform: translate(-200%, 0) rotate(90deg);
	transform-origin: 100% 100%;
	transition: transform 2s;
}

.curious {
	transform: translate(-110%, 0) rotate(90deg);
}

</style>