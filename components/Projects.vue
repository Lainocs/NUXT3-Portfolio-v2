<template>
	<div id="projects">
		<h2>2. Some projects</h2>
		
		<div class="project" v-for="project in projects" :key="project.name">
			<div class="project-content">
				<h3>{{ project.name }}</h3>
				<p>• {{ project.description }}</p>
			</div>
			<img :src="project.image" :alt="project.title">
			<a v-if="project.link" :href="project.link">See project</a>
		</div>

		<img src="deco/constellation.png" alt="constellation">

		<span>More on <a href="https://www.github.com/Lainocs">GitHub</a>...</span>

	</div>
</template>

<script>
	export default {
		name: 'ProjectsComponent',
		data() {
			return {
				projects: [
					{
						name: 'Forum Associatif Numérique',
						language: "Symfony",
						description: "Répertorier les associations du pôle Léonard de Vinci",
						image: "forum.png",
						link: "https://forum-associatif-numerique.fr"
					},
					{
						name: 'Forum Associatif Numérique',
						language: "Symfony",
						description: "Répertorier les associations du pôle Léonard de Vinci",
						image: "forum.png",
						link: "https://forum-associatif-numerique.fr"
					},
				]
			}
		},
	}
</script>

<style>
	#projects {
		width: 80%;
		margin: 20rem auto 0 auto;
		position: relative;
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	#projects > img {
		width: 50%;
		position: absolute;
		left: 0;
		top: 20rem;
	}

	#projects h2 {
		font-size: 2rem;
		font-weight: 300;
		margin: 4rem 0;
		letter-spacing: 0.5rem;
		text-align: right;
	}

	.project {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: flex-start;
		position: relative;
		margin: 5rem 0;
	}

	.project-content {
		padding: 20px;
		min-height: 150px;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		margin: 10px 0;
	}

	.project:nth-child(2n+1) {
		text-align: right;
		align-items: flex-end;
	}

	.project-content h3 {
		font-size: 1.5rem;
		font-weight: 500;
		margin: 0;
	}

	.project-content p {
		font-size: 1rem;
		font-weight: 300;
		margin: 0;
	}

	.project img {
		border-radius: 10px;
		border: 3px solid var(--color-text);
	}

	.project a {
		position: absolute;
		bottom: 0;
		right: 0;
		padding: 10px;
		background-color: var(--color-primary);
		border: 3px solid var(--color-text);
		border-radius: 10px;
		transition: 1s;
	}

	#projects span {
		font-size: 3rem;
		font-weight: 300;
		margin: 4rem auto;
		text-align: center;
		letter-spacing: 1rem;
	}

	#projects span a {
		color: var(--color-secondary);
		transition: 1s;
		border-bottom: 3px dashed var(--color-secondary);
	}

	#projects span a:hover {
		color: var(--color-text);
		transition: 1s;
		border-bottom: 3px dashed var(--color-text);
	}

	@media screen and (min-width: 1100px) {
		.project-content {
			position: absolute;
			background-color: var(--color-primary);
			border: 3px solid var(--color-text);
			border-radius: 10px;
			width: 50%;
		}
		
		.project img {
			width: 50%;
		}
		
		.project:nth-child(2n+1) .project-content {
			left: 100px;
			text-align: left;
		}

		.project:nth-child(2n) .project-content {
			right: 100px;
			text-align: right;
		}

		.project:nth-child(2n+1) a {
			left: 300px;
			right: auto;
		}

		.project:nth-child(2n) a {
			right: 300px;
			left: auto;
		}

		.project a:hover {
			background-color: var(--color-secondary);
			transition: 1s;
		}
	}
</style>