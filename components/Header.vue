<template>
	<div id="header">
		<nav>
			<ul>
				<li>About</li>
				<li>Projects</li>
				<li>Contact</li>
			</ul>
		</nav>
		<div class="header-content">
			<div class="header-images">
				<img src="deco/vector.png" alt="vector">
				<img src="nico.png" alt="Nicolas de Garrigues">
			</div>
			<div class="header-text">
				<h1>Nicolas <br> de Garrigues</h1>
				<span>Web Developer</span>
			</div>
		</div>
	</div>
</template>
<script>
	export default {
		name: 'HeaderComponent'
	}
</script>

<style>
	#header {
		position: relative;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: center;
		padding: 2rem 0;
		height: 100vh;
	}

	#header nav {
		width: 100%;
		display: flex;
		justify-content: center
	}

	#header nav ul {
		display: flex;
		flex-direction: column;
		gap: 20px;
		text-align: center;
		list-style: none;
	}

	#header nav ul li {
		font-size: 1.5rem;
		font-weight: 600;
		cursor: pointer;
	}

	#header .header-images {
		height: 100%;
		display: flex;
		flex-direction: column;
		align-items: center;
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		width: 100%;
	}

	#header .header-images img {
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
	}

	#header .header-images img:first-child {
		width: 70%;
	}

	#header .header-images img:last-child {
		width: 80%;
	}

	#header .header-text {
		display: flex;
		flex-direction: column;
		align-self: flex-start;
		z-index: 2;
	}

	#header .header-text h1 {
		font-size: 3rem;
		font-weight: 600;
	}

	#header .header-text span {
		font-size: 1.5rem;
		font-weight: 600;
		color: var(--color-secondary);
	}

	@media screen and (min-width: 950px) {

		#header nav {
			justify-content: flex-end;
		}

		#header nav ul {
			flex-direction: row;
			gap: 50px;
		}

		/* hover animation underline */
		#header nav ul li {
			position: relative;
		}

		#header nav ul li::after {
			content: '';
			position: absolute;
			bottom: -5px;
			left: 0;
			width: 0%;
			height: 2px;
			background-color: var(--color-secondary);
			transition: 0.5s;
		}

		#header nav ul li:hover::after {
			width: 100%;
		}

		#header .header-content {
			width: 100%;
			display: flex;
			justify-content: space-between;
			align-items: flex-end;
		}

		#header .header-images {
			order: 2;
			align-items: flex-end;
			position: initial;
			transform: none;
			width: 50%;
		}

		#header .header-images img {
			bottom: 0;
			right: 0;
			top: initial;
			left: initial;
			transform: none;
		}

		#header .header-images img:first-child {
			width: 60%;
		}

		#header .header-images img:last-child {
			width: 70%;
		}

		#header .header-text {
			align-self: flex-end;
			width: 70%;
		}

		#header .header-text h1 {
			font-size: 5rem;
		}

		#header .header-text span {
			font-size: 3rem;
		}
	}

</style>