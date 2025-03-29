<script>
    // const {onFlipAuthCard} = $props();
</script>



<h2>Sign in</h2>
<form id="signin-card">
    <label for="username">Username</label>
    <input id="username" type="text" placeholder="your username..." required>

    <label for="create-password">Create password</label>
    <input id="create-password" type="password" placeholder="create your password..." required>

    <button type="submit">Sign in</button>
</form>

<p>Dont have an account? <span onclick={onFlipAuthCard}>Sign up</span></p>

