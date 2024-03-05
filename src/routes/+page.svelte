<script>
	import arrow from '$lib/images/Arrow.png';
	import { page } from '$app/stores';

	// const scrollThreshold = 100;
	//
	// function handleNavigation() {
	// 	if (window.scrollY > scrollThreshold) {
	// 		console.log('navigating to home');
	// 	}
	// }
	//
	// onMount(() => {
	// 	window.addEventListener('scroll', handleNavigation);
	//
	// 	return () => {
	// 		window.removeEventListener('scroll', handleNavigation);
	// 	};
	// });
</script>

<svelte:head>
	<title>Landing</title>
	<meta name="description" content="Landing Page" />
</svelte:head>
<body class="landing">
	<div class="link">
		<a href="/home" aria-current={$page.url.pathname === '/'}> byong </a>
	</div>
	<div class="image">
		<img src={arrow} alt="arrow" class="arrow" />
	</div>
</body>

<style>
	.landing {
		background-image: url('$lib/images/byongbg.png');
		background-size: cover;
		background-position: center;
		display: flex;
		justify-content: center; /* Horizontally center content */
		align-items: center; /* Vertically center content */
		height: 100vh; /* Set the height to fill the viewport */
	}

	.container {
		text-align: center; /* Center text within container */
	}

	.link {
		margin-bottom: 20px; /* Add some space between the link and the image */
	}

	.image {
		display: flex; /* Ensure the image is centered properly */
		justify-content: center; /* Center the image horizontally */
	}

	.image img {
		max-width: 100%; /* Ensure the image doesn't exceed container width */
	}

	a {
		color: #fff;
		font-size: 50px;
		font-weight: normal; /* Adjust font weight as needed */
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
		overflow: hidden;
		background-image: transparent; /* Ensure body has no background */
	}
</style>
