<script>
export let option = 0;

function handleClickInterests() {
  option = 1
}

function handleClickSkills() {
  option = 2
}

</script>


  <div class="display"> 

    <div class="card-container">
      
      <span class="card card-1">
        <h2>INTERESTS</h2>
        <p>Things you'll find me doing in my free time.</p>
        <button 
        on:click|preventDefault="{handleClickInterests}"
        >
        Giphy Mode
        </button>
      </span>
        
      <span class="card card-2">
        <h2>SKILLS</h2>
        <p>Skills I have, am actively learning or will be pursuing.</p>
        <button 
        on:click|preventDefault="{handleClickSkills}"
        >
        Giphy Mode
        </button>
      </span>

    </div>

    {#if option === 0}
    <h3>I'm Carlos! I love people<br> technology<br> and aim to make the world<br> a better place.</h3>
    <a href="https://www.linkedin.com/in/carlos-german-a56b60217/">
    <img a class="ln" src="lnlogo.png" alt="linkedin">
    </a>
    {:else if option === 1 }  
    <div class="gif-row">
      <img src="https://media.giphy.com/media/l2SpUepuM4qgdzbeU/giphy.gif" class="gifs" alt="cats">
      <img src="https://media.giphy.com/media/vsyKKf1t22nmw/giphy.gif" class="gifs" alt="cats">
      <img src="https://media.giphy.com/media/cFdHXXm5GhJsc/giphy.gif" class="gifs" alt="cats">
      <img src="https://media.giphy.com/media/l1TJTwU3VfPHU4FCbx/giphy.gif" class="gifs" alt="cats">
      <img src="https://media.giphy.com/media/pO4UHglOY2vII/giphy.gif" class="gifs" alt="cats">
    </div>
    {:else if option === 2 }
    <div class="gif-row">
      <img src="https://media.giphy.com/media/xT9IgzoKnwFNmISR8I/giphy.gif" class="gifs" alt="cats">
      <img src="https://media.giphy.com/media/coxQHKASG60HrHtvkt/giphy.gif" class="gifs" alt="cats">
      <img src="https://media.giphy.com/media/3og0ICG4WxdKSRzE3K/giphy.gif" class="gifs" alt="cats">
      <img src="https://media.giphy.com/media/3o7qE1EaTWLQGDSabK/giphy.gif" class="gifs" alt="cats">
      <img src="https://media.giphy.com/media/13FrpeVH09Zrb2/giphy.gif" class="gifs" alt="cats">
    </div>
    {/if}
  </div>

<style>
  .ln {
    margin: 0.5em;
    object-fit: cover;
    border-radius:50%;
    width: 75px;
    height: 75px;
  }

  p {
    color: rgba(92, 88, 94, 0.897);
  }
  h2 {
    font-weight: 200;
    color: rgba(152, 91, 202, 0.808);
  }

  h3 {
		color: #ecddf7;
		text-transform: uppercase;
		font-size: 1.5em;
		font-weight: 200;
    padding: 1.5em;
    font-family:'Roboto',sans-serif;
    line-height: 1.5em;
    text-shadow: 1px 1px 4px #525252;
	}

  button {
    display: inline-block;
    padding: 0.35em 1.2em;
    border:0.1em solid #e9b0fa;
    margin:0 0.3em 0.3em 0;
    border-radius: 0.12em;  
    box-sizing: border-box;
    text-decoration: none;
    font-family:'Roboto',sans-serif;
    font-weight:300;
    color:#161616;
    text-align:center;
    transition: all 0.2s;  
  }

  button:hover {
    color: rgb(255, 255, 255);
    background-color: rgba(222, 135, 193, 0.733);
    font-family:'Roboto',sans-serif;
    border: #fdf8ff 0.1em solid;
  }
  

  .gif-row {
    padding: 1.5em;
    margin-top: 2em;
  }

  img {
    width: 250px;
    height: 250px;
    border-radius: 10px;
    padding: 5px;
    object-fit: cover;
    border-radius: 1em;
  }

  .display {
    display: inline-block;
    justify-content: center;
    width: 100%;
    vertical-align: bottom;
  }
  
  .card-container {
    margin-top: 1.5em;
    display: block;
    object-position: fixed;
    justify-content: center;
    width: 100%;
  }

  .card {
    background: rgba(255, 255, 255, 0.548);
    display: inline-block;
    border-radius: 1em;
    width: 200px;
    height: 200px;
    box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
    padding: 1em;
    margin: 1em;
    vertical-align: auto;
    transition: all .2s ease-in-out;
  }

  .card:hover {
  box-shadow: 0 14px 28px rgba(0,0,0,0.25), 0 10px 10px rgba(0,0,0,0.22);
  scale: (1.5);
}
</style>