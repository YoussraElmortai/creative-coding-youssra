<script>
	import { gsap } from 'gsap';
	import { ScrollTrigger } from 'gsap/dist/ScrollTrigger';
	import { TextPlugin } from 'gsap/dist/TextPlugin';
    import { onMount } from 'svelte';

	gsap.registerPlugin(ScrollTrigger, TextPlugin);

	 // Function to animate the blob element
  function animateBlob() {
    gsap.to('.blob', {
      duration: 1,
      scale: 1.2, // Scale to 1.2 times its original size
      ease: 'power2.out' // Easing function
    });
  }

  onMount(() => {
    animateBlob(); // Trigger the animation when the component mounts
  });
	
</script>

<header><img src="/logo.png" alt="plantswap"></header>
<section class="banner"></section>
<div class="blob"></div>

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

	 .blob {
    /* Add styles for your blob element */
    width: 100px;
    height: 100px;
    background-color: red; /* Replace with your desired blob styles */
  }

</style>
