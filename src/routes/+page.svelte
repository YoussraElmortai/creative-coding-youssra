<script>
	import { gsap } from 'gsap';
    import { onMount } from 'svelte';
	import Scrollanimation from '$lib/components/Scrollanimation.svelte';

	 onMount(() => {
    const overlay = document.querySelector('.overlay');

    window.addEventListener('mousemove', (e) => {
      const { clientX, clientY } = e;
      const x = Math.round((clientX / window.innerWidth) * 100);
      const y = Math.round((clientY / window.innerHeight) * 100);

      gsap.to(overlay, {
        '--x': `${x}%`,
        '--y': `${y}%`,
        duration: 0.3,
        ease: 'sine.out'
      });
    });
  });
</script>
<!-- week 1 spike -->
<!-- <Scrollanimation></Scrollanimation> -->

<!-- week 2 spike -->

<header >
	<h1>PLANTSWAP JE GEK</h1>
</header>
<!-- dit is de overlay die over de main header wordt gezet -->
<header class="overlay">
	<h1>PLANTSWAP JE GEK</h1>
</header>

<!--week 3 spike-->

<style>
	header{
		height: 100vh;
		padding: 3em;	
	}

	h1{
		font-size: 5rem;
	}

	.overlay{
		color: white;
		background-image: url(https://images.unsplash.com/photo-1457089328109-e5d9bd499191?q=80&w=363&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D);
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;

		clip-path: circle(60px at var(--x, 50%) var(--y,50%));
		transition: clip-path 50ms;
	}


</style>