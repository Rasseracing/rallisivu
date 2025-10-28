<script lang="ts">
	import favicon from "$lib/assets/favicon.svg";

	let { children } = $props();
</script>

<!-- svelte-ignore a11y_missing_attribute -->
<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<nav class="navbar">
	<div class="valikko">
		<a href="/blogi">blogi</a>
		<a href="/videot">vidoita</a>
		<a href="/nuotit">nuotit</a>
		<a href="/kartat"> karttoja</a>
	</div>
	<div class="kirnappi">
		<p>kirjautuminen</p>
	</div>
</nav>

{@render children?.()}

<div class="linkkipalkki">
	<a href="https://www.tiktok.com/@rasseracing">
		<!-- svelte-ignore a11y_missing_attribute -->
		<img class="linkki-logot" id="tk" src="/tiktok.webp" width="50px" /></a
	>
	<a href="https://www.youtube.com/@Rasseracing">
		<!-- svelte-ignore a11y_missing_attribute -->
		<img class="linkki-logot" id="yt" src="/ytkuva.png" width="50px" />
	</a>
	<a href="https://www.instagram.com/rasseracing/">
		<!-- svelte-ignore a11y_missing_attribute -->
		<img
			class="linkki-logot"
			id="iglogo"
			src="/iglogo.png"
			width="50px"
		/></a
	>
</div>

<style>
	:global(body) {
		margin: 0;
		padding: 0;
	}
	.navbar {
		display: flex;
		justify-content: space-between;
		background-color: orange;
		padding-right: 30px;
	}

	.navbar a {
		text-decoration: none;
	}
	.navbar a:hover {
		color: blueviolet;
	}
	.valikko {
		display: flex;
		text-indent: 10px;
	}
	.linkkipalkki {
		position: absolute;
		bottom: 0px;
		display: flex;
		justify-content: center;
		width: 100vw;
		border-top: 1px solid black;
		align-items: center;
	}

	.linkki-logot {
		display: block;
	}
</style>
