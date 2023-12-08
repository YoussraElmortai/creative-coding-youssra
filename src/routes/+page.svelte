<script>
	import { gsap } from 'gsap';
	import { ScrollTrigger } from 'gsap/dist/ScrollTrigger';
	import { TextPlugin } from 'gsap/dist/TextPlugin';
    import { onMount } from 'svelte';

	gsap.registerPlugin(ScrollTrigger, TextPlugin);

	 
	// function to scrolltrigger trigger something
  function animateScroll() {
    gsap.to('.info', {
      duration: 1,
	  x: 1000,
	  y: 100,
	  scrollTrigger:{
		trigger:'.wrapper',
		start: 20,
		end: 110,
		scrub: 2,
		toggleActions:'restart none none none'
	  },
	  stagger:0.1,

    });
	
  }


  onMount(() => {
    animateScroll(); // Trigger the animation when the component mounts
  });
	
</script>
<header><img src="/logo.png" alt="plantswap"></header>

<section class="wrapper">
	<section class="info">
	<p>In the Aftermath: Seeking Salvation in a Nuclear Wasteland, Discovering Healing Plants Amidst the Undead Horde</p>
	</section>
	<section class="info">
		<p>In the Aftermath: Seeking Salvation in a Nuclear Wasteland, Discovering Healing Plants Amidst the Undead Horde</p>
	</section>
</section>



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

	.wrapper{
		height: 100vh;
		width: 100%;
		overflow-x: hidden;
	}

  .info p{
	position: relative;
	top: -100px;
	left: -850px;
	right: 200px;
	width: 60vw;
	font-size: 20px;
	background-color: var(--card-background);
	border-radius: 10px;
	padding: 1rem;
	margin: 1rem;
	margin-top: 5rem;
  }

  .info p:hover{
	color: var(--card-background);
  }



</style>
