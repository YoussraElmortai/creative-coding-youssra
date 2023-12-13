<script>
    import { gsap } from 'gsap';
    import { onMount } from 'svelte';

    onMount(() => {
    const overlay = document.querySelector('.overlay');

    window.addEventListener('mousemove', (e) => {
      const { clientX, clientY } = e;
      const x = Math.round((clientX / window.innerWidth) * 100);
      const y = Math.round((clientY / window.innerHeight) * 100);

	    overlay.style.setProperty('--x', `${x}%`);
        overlay.style.setProperty('--y', `${y}%`);

      gsap.to(overlay, {
        '--x': `${x}%`,
        '--y': `${y}%`,
        duration: 0.3,
        ease: 'sine.out'
      });
    });
  });
</script>

<header >
	<h1>PLANTSWAP JE GEK</h1>
	<a href="/">start met swappen</a>
</header>
<!-- dit is de overlay die ov de main header wordt gezet -->
<header class="overlay">
	<h1>PLANTSWAP JE GEK</h1>
	<a href="/">start met swappen</a>
</header>

<style>
	header{
		height: 100%;
		width: 100%;
		padding: 2em;
		overflow: hidden;	
	}

	h1{
		font-size: 5rem;
		margin-bottom: 2rem;
	}

	a{
		text-decoration: none;
		color: black;
		font-size: 2rem;
		background-color: darkcyan;
		padding: 0.5rem;
		border-radius: 6px;
		width: 20rem;
	}


@keyframes clipAnimation {
	0% {
		clip-path: circle(0% at var(--x, 50%) var(--y, 50%));
	}
	25% {
		clip-path: circle(100vw at var(--x, 50%) var(--y, 50%));
	}
	50% {
		clip-path: circle(30px at var(--x, 50%) var(--y, 50%));
	}
	75% {
		clip-path: circle(180px at var(--x, 50%) var(--y, 50%));
	}
	100% {
		clip-path: circle(120px at var(--x, 50%) var(--y, 50%));
	}
}

	.overlay{
		color: white;
		background-image: url(https://images.unsplash.com/photo-1584727638057-78254f636b5a?q=80&w=1976&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D);
		background-size: cover;
		position: absolute;
		top: 0;
		left: 0;
		width: 100%; 
		/* mask: url(https://static.thenounproject.com/png/3342460-200.png);
		-webkit-mask: url(https://static.thenounproject.com/png/3342460-200.png);   */
		clip-path: circle(120px at var(--x, 50%) var(--y,50%));
		animation: clipAnimation 4s  ;
		transition: clip-path  0.3s cubic-bezier(0.61, 1, 0.88, 1);
	}

	.overlay a{
		color: white;
		background-color: plum;
	}


</style>