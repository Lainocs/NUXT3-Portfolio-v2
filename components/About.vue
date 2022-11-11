<template>
	<div id="about">
		<h2>1. Who am I ?</h2>
		<div>
			<img class="fusee" src="deco/fusee.png" alt="fusee">
			<p>Currently student but also teacher and founding president of the association La 404 DeVinci, I am passionate about the world of digital and more particularly the development of websites and applications.</p>
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
		text-align: justify;
	}

	#about .fusee {
		width: 50%;
		position: absolute;
		top: 50px;
		right: 0;
		z-index: -1;
	}

	#about .skills {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		justify-content: space-around;
	}

	#about .skills span {
		font-size: 1.5rem;
		text-align: center;
		width: 200px;
		font-weight: 600;
		margin: 1rem 0;
		border: 1px solid var(--color-text);
		padding: 1rem;
		border-radius: 5px;
		transition: 1s;
		cursor: pointer;
	}

	#about .skills span:first-child {
		background-color: var(--javascript);
		color: black;
	}

	#about .skills span:nth-child(2) {
		background-color: var(--laravel);
		color: white;
	}

	#about .skills span:nth-child(3) {
		background-color: var(--php);
		color: black;
	}

	#about .skills span:nth-child(4) {
		background-color: var(--vuejs);
		color: white;
	}

	@media screen and (min-width: 950px) {
		#about p {
			font-size: 2rem;
		}

		#about .skills span:first-child, #about .skills span:nth-child(2), #about .skills span:nth-child(3), #about .skills span:nth-child(4) {
			/* remove bg color */
			background-color: transparent;
			color: var(--color-text);
		}

		/* hover skills */
		#about .skills span:first-child:hover {
			background-color: var(--javascript);
			color: black;
			transition: 1s;
		}

		#about .skills span:nth-child(2):hover {
			background-color: var(--laravel);
			color: white;
			transition: 1s;
		}

		#about .skills span:nth-child(3):hover {
			background-color: var(--php);
			color: black;
			transition: 1s;
		}

		#about .skills span:nth-child(4):hover {
			background-color: var(--vuejs);
			color: white;
			transition: 1s;
		}
	}
</style>