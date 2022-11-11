<template>
	<div id="page">
		<Header />
		<Presentation />
		<About />
	</div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>

<style>
:root {
	--background-color: rgba(1,3,24,1);
	--color-primary: #010318;
	--color-secondary: #404C6C;
	--color-text: #7B86A1;
}

/* put background color and background image must have 0.1 opacity */
body {
	font-family: 'Poppins', sans-serif;
	background-color: var(--background-color);
	background-repeat: repeat;
	background-size: 30%;
	background-position: center;
}

body::after {
	content: '';
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	height: 300vh;
	background-image: url('/deco/stars.png');
	z-index: -1;
	opacity: 0.1;
}

#page {
	width: 90%;
	margin: 0 auto;
	opacity: 1;
	color: var(--color-text);
}


</style>
