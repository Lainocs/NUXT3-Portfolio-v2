<template>
	<div id="presentation">
		<h2>Your french made <br> website</h2>
		<img src="deco/vector_circle.png" alt="vector">

		<img class="arrow" src="deco/arrow.png" alt="arrow">

		<div class="presentation-projects">
			<img src="pres-projects/forum.png" alt="forum">
			<img src="pres-projects/competences.png" alt="competences">
			<img src="pres-projects/api.png" alt="api">
		</div>
	</div>
</template>
<script>
	export default {
		name: 'PresentationComponent'
	}
</script>

<style>
	#presentation {
		margin-top: 100px;
		display: flex;
		flex-direction: column;
		align-items: center;
		position: relative;
	}

	#presentation h2 {
		width: 100%;
		font-size: 4rem;
		font-weight: 300;
		margin: 4rem auto;
		text-align: center;
		letter-spacing: 1rem;
	}

	#presentation > img {
		width: 50%;
		position: absolute;
		left: 35%;
		top: 50px;
	}

	#presentation .arrow {
		width: 50px;
		position: absolute;
		left: 20%;
		top: 450px;
	}

	#presentation .presentation-projects {
		margin-top: 100px;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		width: 100%;
	}

	#presentation .presentation-projects img {
		width: 50%;
		margin: 0 auto;
	}

	#presentation .presentation-projects img:nth-child(2) {
		margin: -30px 15%;
	}

	#presentation .presentation-projects img:nth-child(3) {
		margin: -30px 40%;
	}

	@media screen and (min-width: 950px) {

		#presentation h2 {
			width: 50%;
		}
		#presentation .arrow {
			top: 400px;
		}

		#presentation .presentation-projects img {
			width: 40%;
		}

		#presentation .presentation-projects img:nth-child(2) {
			margin: -80px 15%;
		}

		#presentation .presentation-projects img:nth-child(3) {
			margin: -80px 40%;
		}
	}

</style>