<!-- LandingPage.svelte -->
<script>
	export let pageTitle = 'Landing Page';
	import { page } from '$app/stores';
</script>

<svelte:head>
	<title>{pageTitle}</title>
	<meta name="description" content="Landing Page" />
</svelte:head>

<body class="landing">
	<a href="/home" aria-current={$page.url.pathname === '/'}> byong </a>
</body>

<style>
	a {
		color: white; /* Set link color to white */
		font-size: 45px; /* Adjust font size */
		text-decoration: none;
	}
	@font-face {
		font-family: 'Marcellus';
		font-style: normal;
		font-weight: normal; /* Adjust font weight as needed */
		src: url('../lib/fonts/Marcellus-Regular.ttf') format('truetype'); /* Adjust the font file path and format */
	}

	body {
		font-family: 'Marcellus', sans-serif;
		background-color: black;
		margin: 0; /* Remove default body margin */
		padding: 0; /* Remove default body padding */
		overflow-x: hidden; /* Hide horizontal scrollbar */
	}
	.landing {
		background-image: url('../lib/images/byongbg.png');
		background-repeat: no-repeat;
		background-attachment: fixed;
		background-position: center;
		background-size: cover;
		display: flex;
		align-items: center;
		justify-content: center;
		height: 100vh;
		overflow: hidden;
	}
</style>
