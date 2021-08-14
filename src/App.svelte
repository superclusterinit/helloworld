<script>
  import Nav from "./Nav.svelte";
  import AboutMe from "./AboutMe.svelte";
  import Ken from "./Ken.svelte";
  import Kimchi from "./Kimchi.svelte"
  import Built from "./Built.svelte";
</script>




<body>
  <div class="bodywrapper">
  <Nav />
  <main>
    <AboutMe />
    <Ken />
    <Kimchi />
    <Built />
  </main>
</div>
</body>




<style>

  body {
    margin: auto 0;
    border-radius: 1em;
  }


  .bodywrapper {
    background-image: url("https://media.giphy.com/media/TxVVB6PfWMjE4/giphy.gif");
    background-attachment: fixed;
    font-family:'Roboto', sans-serif;
    font: 1em/1.3;
    margin: 0 auto;
    min-height: 100%;
    background-repeat: no-repeat;
    background-size: cover;
    padding: 1.5em;
    width: 100%;
    margin-left: auto;
    margin-right: auto;
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
    object-position: center;
    justify-content: center;
	}

	@media (min-width: 640px) {
    body {
      height: 100%;
      min-height: 100%;
    }
		main {
			max-width: none;
		}
	}
</style>