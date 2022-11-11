<template>
	<div id="about">
		<h2>1. Who am I ?</h2>
		<div>
			<img class="fusee" src="deco/fusee.png" alt="fusee">
			<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Laboriosam natus, dicta dolorum non voluptate nemo tempore, alias officia accusantium nihil tenetur rerum debitis in. Repellat asperiores vel molestias earum rerum?</p>
			<div class="skills">
				<span>Javascript</span>
				<span>Laravel</span>
				<span>PHP</span>
				<span>VueJS</span>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'AboutComponent'
	}
</script>

<style>
	#about {
		width: 80%;
		margin: 20rem auto 0 auto;
		position: relative;
	}

	#about h2 {
		font-size: 2rem;
		font-weight: 300;
		margin: 4rem 0;
		letter-spacing: 0.5rem;
	}

	#about p {
		font-size: 1rem;
		font-weight: 300;
		margin: 4rem 0;
	}

	#about .fusee {
		width: 50%;
		position: absolute;
		top: 50px;
		right: 0;
	}

	#about .skills {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		justify-content: center;
		gap: 2rem;
	}

	#about .skills span {
		font-size: 2rem;
		text-align: center;
		width: 200px;
		font-weight: 300;
		margin: 1rem 0;
		border: 1px solid var(--color-text);
		padding: 1rem;
		border-radius: 5px;
	}

	#about .skills span:hover {
		background-color: var(--color-text);
		color: var(--color-background);
	}

	@media screen and (min-width: 950px) {
		#about p {
			font-size: 2rem;
		}
	}
</style>