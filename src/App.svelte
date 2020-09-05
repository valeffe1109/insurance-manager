<script lang="ts">
import { setContext } from 'svelte'
let email ; 
let password;
const handleSubmit = () => {
	console.log(email,password)
}
</script>

<style lang="scss">
  @import "../node_modules/bulma/bulma.sass";
</style>

<main>
  <nav class="navbar" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
      <a class="navbar-item" href="https://bulma.io">
      </a>

      <a
        role="button"
        class="navbar-burger burger"
        aria-label="menu"
        aria-expanded="false"
        data-target="navbarBasicExample">
        <span aria-hidden="true" />
        <span aria-hidden="true" />
        <span aria-hidden="true" />
      </a>
    </div>

    <div id="navbarBasicExample" class="navbar-menu">
      <div class="navbar-start">
        <a class="navbar-item"> Home </a>

        <a class="navbar-item"> Documentation </a>

        <div class="navbar-item has-dropdown is-hoverable">
          <a class="navbar-link"> More </a>

          <div class="navbar-dropdown">
            <a class="navbar-item"> About </a>
            <a class="navbar-item"> Jobs </a>
            <a class="navbar-item"> Contact </a>
            <hr class="navbar-divider" />
            <a class="navbar-item"> Report an issue </a>
          </div>
        </div>
      </div>

      <div class="navbar-end">
        <div class="navbar-item">
          <div class="buttons">
            <a class="button is-primary"> <strong>Sign up</strong> </a>
            <a class="button is-light"> Log in </a>
          </div>
        </div>
      </div>
    </div>
  </nav>

  <div class="container mt-6">
   <form on:submit|preventDefault ={handleSubmit}>
  <div class="field">
 
  <label class="label">Email</label>
  <div class="control">
    <input class="input" type="text" name="email" placeholder="Text input" bind:value={email}>
  </div>
</div>
  <div class="field">
  <label class="label">Password</label>
  <div class="control">
    <input class="input" type="password" name="password" placeholder="Text input"  bind:value={password}>
  </div>
</div>
<div class="field is-grouped">
  <div class="control">
    <button class="button is-link" >Submit</button>
  </div>
</form>
</div>
  
</main>
