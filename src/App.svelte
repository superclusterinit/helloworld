<script>
  import Nav from "./Nav.svelte";
  import AboutMe from "./AboutMe.svelte";
</script>




<body>
  <Nav />
  <main>
    <AboutMe />


  </main>
</body>




<style>

  

  body {
    font-family:'Roboto',sans-serif;
    background: linear-gradient(-45deg, #a352ee, #bbbbbb, #4197b6, #4c318d);
    background-size: 400% 400%;
    animation: gradient 15s ease infinite;
    width: 100%;
    font: 1em/1.3;
    margin: 0 auto;
  }

  @keyframes gradient {
    0% {
      background-position: 0% 50%;
    }
    50% {
      background-position: 100% 50%;
    }
    100% {
      background-position: 0% 50%;
    }
  }

	main {
		text-align: center;
    font-family:'Roboto',sans-serif;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>