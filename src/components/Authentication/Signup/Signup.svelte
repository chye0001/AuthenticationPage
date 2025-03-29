<script>
    // const {onFlipAuthCard} = $props();
</script>



<h2>Sign up</h2>
<form id="signup-card">
    <label for="username">Username</label>
    <input id="username" type="text" placeholder="your username..." required>

    <label for="email">Email</label>
    <input id="email" type="email" placeholder="enter your email..." required>

    <label for="create-password">Create password</label>
    <input id="create-password" type="password" placeholder="create your password..." required>

    <label for="confirm-password">Confirm password</label>
    <input id="confirm-password" type="password" placeholder="confirm your password..." required>

    <button type="submit">Sign up</button>
</form>

<p>Already have an account? <span onclick={onFlipAuthCard}>Sign up</span></p>
