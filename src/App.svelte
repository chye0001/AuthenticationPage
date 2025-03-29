<script>
  import Signin from './components/Authentication/Signin/Signin.svelte';
  import Signup from './components/Authentication/Signup/Signup.svelte';

  let flipped = $state(false);
</script>

<div id="container">

  <button
  class={["card", { flipped }]}
		onclick={() => flipped = !flipped}
  >
    <div class="signup">
      <Signup/>
    </div>
  
    <div class="signin">
      <Signin/>
    </div>

  </button>
</div>

<style>
  /* #authentication-card {
      width: 300px;
      padding: 20px;
      background: whitesmoke;
      box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
      border-radius: 10px;
      border: 1px solid gray;
      text-align: center;
  } */

  /* FROM SVELTE DOCS CARD FLIP */
  .container {
		display: flex;
		flex-direction: column;
		gap: 1em;
		height: 100%;
		align-items: center;
		justify-content: center;
		perspective: 100vh;
	}

	.card {
		position: relative;
		aspect-ratio: 2.5 / 3.5;
		font-size: min(1vh, 0.25rem);
		height: 80em;
		background: var(--bg-1);
		border-radius: 2em;
		transform: rotateY(180deg);
		transition: transform 0.4s;
		transform-style: preserve-3d;
		padding: 0;
		user-select: none;
		cursor: pointer;
	}

	.card.flipped {
		transform: rotateY(0);
	}

	.signin, .signup {
		display: flex;
		align-items: center;
		justify-content: center;
		position: absolute;
		width: 100%;
		height: 100%;
		left: 0;
		top: 0;
		backface-visibility: hidden;
		border-radius: 2em;
		border: 1px solid var(--fg-2);
		box-sizing: border-box;
		padding: 2em;
	}

	.signin {
		background: url(./svelte-logo.svg) no-repeat 5em 5em, url(./svelte-logo.svg) no-repeat calc(100% - 5em) calc(100% - 5em);
		background-size: 8em 8em, 8em 8em;
	}

	.signup {
		transform: rotateY(180deg);
	}
</style>