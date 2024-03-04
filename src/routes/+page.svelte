<script>
	import arrow from '$lib/images/Arrow.png';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Landing Page" />
</svelte:head>
<body>
	<div class="container">
		<h1>byong</h1>
	</div>
	<div class="image">
		<img src={arrow} alt="arrow" class="arrow" />
	</div>
</body>

<style>
	:global(body) {
		background-color: black;
		background-image: url('$lib/images/byongbg.png');
		background-size: cover;
	}
	.image img {
		margin: auto;
	}
	.image {
		display: flex;
		justify-self: center;
	}

	.container {
		display: flex;
		height: 90vh;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	h1 {
		color: #fff;
		font-size: 50px;
		font-weight: normal; /* Adjust font weight as needed */
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
	}
</style>
