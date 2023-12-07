<script>
	import { gsap } from 'gsap';
	import { ScrollTrigger } from 'gsap/dist/ScrollTrigger';
	import { TextPlugin } from 'gsap/dist/TextPlugin';
    import { onMount } from 'svelte';

	gsap.registerPlugin(ScrollTrigger, TextPlugin);

	 
	// function to scrolltrigger trigger something
  function animateScroll() {
    gsap.to('.info', {
      duration: 1.5,
	  x: 70,
	  y: 10,
	  scrollTrigger:{
		trigger:'.info',
		markers: true,
		start: 20,
		end: 110,
		scrub: 2,
		toggleActions:'restart none none none'
		//   one enter  onleave onenterback onleaveback
	  }
    });
	
  }


  onMount(() => {
    animateScroll(); // Trigger the animation when the component mounts
  });
	
</script>
<!-- <div class="blob"></div> -->
<header><img src="/logo.png" alt="plantswap"></header>

<section class="wrapper">
	<section class="info">
	<p>In the Aftermath: Seeking Salvation in a Nuclear Wasteland, Discovering Healing Plants Amidst the Undead Horde</p>
</section>
<section class="info-2">
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
	width: 60vw;
	font-size: 20px;
	background-color: var(--card-background);
	border-radius: 10px;
	padding: 1rem;
	margin: 1rem;
  }

   .info-2 p{
	width: 60vw;
	font-size: 20px;
	background-color: var(--card-background);
	border-radius: 10px;
	padding: 1rem;
	margin: 1rem;
  }

</style>
