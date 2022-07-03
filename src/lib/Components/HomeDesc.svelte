<div
	class="container relative mx-auto justify-center -z-30"
	>
	<div
		class="card"
		>
		<h1 class="underline">Welcome To My Website</h1>
		<p>Welcome to my website! If you aren't sure about why I have created this then I reccomend you see the about page.</p>
	</div>
	<div
		class="card"
		>
		<h2 class="underline">Enjoy The Site!</h2>
		<p>This is the first website that I have created. The first time I've taught myself how to code infact! Therefore, I welcome you to explore my website in the hopes that you learn something new about me and what I've created through my independant learning.</p>
	</div>
</div>


<style lang="postcss">

	.container{
		@apply bg-slate-200;
		width: auto;
		height: auto;
		border-radius: 20px;
		display: flex;
		flex-direction: raw;
		gap: 20%;
		padding: 40px 0px;
		@apply animate-pulse;
		animation-iteration-count: 1;
		
	}
	.card{
		@apply bg-slate-50;
		width: 40%;
		max-width: 1000px;
		height: auto;
		border-radius: 30px;
		padding: 30px 30px;


	}


	@media screen and (max-width: 800px) {
		.container{
			flex-direction: column;
            padding: 10px 10px;
            
		}

		.card{
			width: auto;
			height: auto;
			padding: 15px 15px;
		}
	}
    @media screen and (min-width:800px){
        .container{
            @apply -top-60;
        }
    }

</style>