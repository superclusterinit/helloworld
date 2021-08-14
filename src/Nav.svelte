<script>
import { onMount } from "svelte";
import { fade } from 'svelte/transition';

const words = [
  "My Space",
  "Carlos' Space",
  "His Space"
	];
	
	// Returns random number for next index.
	const randomSelection = () => {
			return Math.round(Math.random() * (words.length-1)); 
	};
	
	// 	Set `randIndex` to a random value. This will change as it updates.
	let randIndex = randomSelection();
	
	// 	Change interval (milliseconds) here.
	const intervalMS = 1000;
	
	
	// Start the event on mount.  Each interval, the `randIndex` value will update.
	onMount(() => {
		const interval = setInterval(() => {
			// Set `randIndex` to a new value each interval.
			randIndex = randomSelection();
		}, intervalMS);
		return () => {
			clearInterval(interval);
		};		
	});
</script>

<header class="header">
  {#key randIndex}
  <nav class="nav">
    <img 
    class="avatar" 
    src="meandchurro.jpg" 
    alt="carlos">
    <h1 id="title" in:fade >{words[randIndex]}</h1>
  </nav>
  {/key}
</header>

<style>

  .header {
    height: 200px;
    height: 100px;
    background: rgba(255, 255, 255, 0.596);
    border-radius: 1em;
    margin-top: 0%;
    position: relative;
    box-shadow: 0 3px 6px rgba(0,0,0,0.16), 0 3px 6px rgba(0,0,0,0.23);
  }

  .avatar {
    margin: 0.5em;
    object-fit: cover;
    border-radius:50%;
    width: 75px;
    height: 75px;
  }

  .nav {
    display: flex;    
    align-items: center;
    justify-content: center;
  }

  #title {
    display: inline-block;
    color: #9900ff;
		text-transform: uppercase;
		font-size: 1.5em;
		font-weight: 400;
    vertical-align: middle;
    text-shadow: 1px 1px 1px #8585857a;
  }
</style>