<script lang="ts">
	import Image from '../lib/Image.svelte';
	let fileRootDir: string = 'images/';
	let fileNames: Array<string> = ['coffee.gif', 'coffee2.gif', 'jp_wood_jointery.gif'];

	let images: Array<string> = [];

	fileNames.map((img: string) => {
		images.push(fileRootDir + img);
	});
</script>

<svelte:head>
	<title>simple.</title>
</svelte:head>

<main>
	<div class="container">
		<div class="card__container">
            <h1 class="title">me</h1>
            <h2><o> I like <a href="">coffee</a> and <a href="">languages <code >??? </code></a></o></h2>
        </div>

		<div class="image__container">
			{#each images as image}
				<Image src={image} desc="some gif" />
			{/each}
		</div>
	</div>
</main>

<style lang="scss">
	// maybe try this font for headers?
	// https://www.1001fonts.com/beon-font.html
	ul li {
		list-style: none;
	}
	div.card__container {
		display: block;
		position: absolute;
		background-color: white;
	}
	div.container {
		display: flex;
		/* flex-wrap: wrap; */
		flex-direction: row-reverse;
	}
	div.image__container {
		display: flex;
		flex-direction: row;
	}

	a { 
		color: black;
		text-decoration: none;
		&:hover {
			color: grey;
		}
	}
</style>
