<script>
	export let open = false;
</script>

<button
	class="p-7 cursor-pointer mr-4 border-none focus:outline-none"
	class:open
	on:click={() => (open = !open)}
>
	<svg width="30" height="10">
		<line id="top" x1="0" y1="2" x2="32" y2="2" />
		<line id="middle" x1="0" y1="12" x2="24" y2="12" />
		<line id="bottom" x1="0" y1="22" x2="32" y2="22" />
	</svg>
</button>

<style lang="postcss">
	svg {
		@apply text-slate-700;
		min-height: 24px;
		transition: transform 0.3s ease-in-out;
	}

	svg line {
		stroke: currentColor;
		stroke-width: 3;
		transition: transform 0.3s ease-in-out;
	}

	button {
		z-index: 20;
	}

	.open svg {
		@apply scale-105;
	
	}

	.open #top {
		transform: translate(6px, 0px) rotate(45deg);
		@apply text-slate-200;
	
	}

	.open #middle {
		opacity: 0;
		
	}

	.open #bottom {
		transform: translate(-12px, 9px) rotate(-45deg);
		@apply text-slate-200;
	
	}
</style>
