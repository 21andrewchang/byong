<!-- HomePage.svelte -->
<script>
	export let pageTitle = 'Home Page';
	import { page } from '$app/stores';
</script>

<svelte:head>
	<title>{pageTitle}</title>
	<meta name="description" content="Home Page" />
</svelte:head>

<body class="home-page">
	<div class="grid-container">
		<div class="container">
			<a class="text" href="/street" aria-current={$page.url.pathname === '/'}>street</a>
			<div id="street" class="button"></div>
		</div>
		<div class="container">
			<a class="text" href="/architecture" aria-current={$page.url.pathname === '/'}>architecture</a
			>
			<div id="architecture" class="button"></div>
		</div>
		<div class="container">
			<a class="text" href="/portrait" aria-current={$page.url.pathname === '/'}>portrait</a>
			<div id="portrait" class="button"></div>
		</div>
		<div class="container">
			<a class="text" href="/bnw" aria-current={$page.url.pathname === '/'}>bnw</a>
			<div id="bnw" class="button"></div>
		</div>
	</div>
</body>

<style>
	.container {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		position: relative;
		width: 400px;
		height: 270px;
	}

	.text {
		z-index: 1;
		position: relative;
		color: white;
		font-size: 20px;
		text-decoration: none;
		opacity: 0;
	}
	.container:hover .text {
		opacity: 1;
	}

	.button {
		width: 400px;
		height: 270px;
		position: absolute;
		top: 0;
		left: 0;
		background-repeat: no-repeat;
		background-position: center;
		background-size: cover;
		transition: filter 0.3s ease;
	}

	.container:hover .button {
		filter: brightness(20%);
	}

	#architecture {
		background-image: url('../../lib/images/architecture.jpg');
	}

	#street {
		background-image: url('../../lib/images/street.jpg');
	}

	#bnw {
		background-image: url('../../lib/images/bnw.jpg');
	}

	#portrait {
		background-image: url('../../lib/images/portrait.jpg');
	}

	@font-face {
		font-family: 'Marcellus';
		font-style: normal;
		font-weight: normal;
		src: url('../../lib/fonts/Marcellus-Regular.ttf') format('truetype');
	}

	.home-page {
		font-family: 'Marcellus', sans-serif;
		display: flex;
		background-color: black;
		align-items: center;
		overflow: hidden;
		justify-content: center;
		height: 100vh;
	}

	.grid-container {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		gap: 5px;
	}
</style>
