<script>
	import { gsap } from 'gsap';
	import { ScrollTrigger } from 'gsap/dist/ScrollTrigger';
	import { TextPlugin } from 'gsap/dist/TextPlugin';
    import { onMount } from 'svelte';

	gsap.registerPlugin(ScrollTrigger, TextPlugin);

	
</script>

<header><img src="/logo.png" alt="plantswap"></header>
<section class="banner"></section>

<style>
	header{
		height: 10vh;
		width: 100%;
		border-bottom: solid 3px var(--card-background);
	}

	header img{
		margin: 1rem;
		background-color: rgba(0, 0, 0, 0);
	}

	.banner{
		height: 10vh;
		width: 100%;
		background-color: var(--card-background);
		border-bottom: solid 3px var(--card-background);
	}

</style>
