<script>
	import { gsap } from 'gsap';
	import { ScrollTrigger } from 'gsap/dist/ScrollTrigger';
	import { TextPlugin } from 'gsap/dist/TextPlugin';
    import { onMount } from 'svelte';

	gsap.registerPlugin(ScrollTrigger, TextPlugin);
</script>

<header><img src="/logo.png"></header>
<section></section>
<section></section>
<section></section>

<style>
	header{
		height: 10vh;
		width: 100%;
		border-bottom: solid 3px var(--card-background);
	}

	header img{
		margin: 1rem;
	}

</style>
