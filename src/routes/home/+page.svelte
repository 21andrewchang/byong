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
	<div class="title">byong</div>
	<div class="grid-container">
		<div class="container">
			<a href="/street" aria-current={$page.url.pathname === '/'} class="button-link">
				<div id="street" class="button"></div>
				<span class="text">street</span>
			</a>
		</div>
		<div class="container">
			<a href="/architecture" aria-current={$page.url.pathname === '/'} class="button-link">
				<div id="architecture" class="button"></div>
				<span class="text">architecture</span>
			</a>
		</div>
		<div class="container">
			<a href="/portrait" aria-current={$page.url.pathname === '/'} class="button-link">
				<div id="portrait" class="button"></div>
				<span class="text">portrait</span>
			</a>
		</div>
		<div class="container">
			<a href="/bnw" aria-current={$page.url.pathname === '/'} class="button-link">
				<div id="bnw" class="button"></div>
				<span class="text">black/white</span>
			</a>
		</div>
	</div>
</body>

<style>
	.title {
		color: white;
		padding-bottom: 5px;
	}
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
		font-size: 10px;
		text-decoration: none;
		opacity: 0;
		font-weight: lighter;
	}
	.container:hover .text {
		opacity: 1;
	}

	.button {
		width: 517px;
		height: 345px;
		position: absolute;
		text-decoration: none;
		top: 0;
		left: 0;
		background-repeat: no-repeat;
		background-position: center;
		background-size: cover;
		transition: filter 0.3s ease;
	}

	.container:hover .button {
		filter: brightness(20%);
		text-decoration: none;
	}
	.button-link {
		display: inline-block;
		text-decoration: none;
	}

	.button-link:hover .button {
		filter: brightness(20%);
	}

	.button-link:hover .text {
		opacity: 1;
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
		font-weight: 200;
		src: url('../../lib/fonts/Marcellus-Regular.ttf') format('truetype');
	}

	.home-page {
		font-family: 'Marcellus', sans-serif;
		display: flex;
		background-color: black;
		align-items: center; /* Align items vertically */
		overflow: hidden;
		justify-content: center;
		height: 100vh;
		flex-direction: column;
		width: 100%;
	}
	body {
		background-color: black; /* Set background color */
		margin: 0; /* Remove default body margin */
		padding: 0; /* Remove default body padding */
		overflow: hidden;
	}

	.grid-container {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		gap: 5px;
	}
</style>
