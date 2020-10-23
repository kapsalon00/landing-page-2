<script>
  import { createEventDispatcher } from "svelte";

  export let login = false;
  export let register = false;
  export let visible = false;

  const dispatch = createEventDispatcher();

  const modalClose = () => {
    dispatch("modalClose");
  };
</script>

<style lang="scss">
  .wrapper {
    z-index: 2;
    position: absolute;
    top: 10%;
    min-width: 300px;
    background-color: white;
    border-radius: 5px;
    box-shadow: 12px 12px 18px -8px rgba(107, 99, 107, 1);
    &::after {
      content: "";
      position: absolute;
      width: 0px;
      height: 0px;
      left: 50%;
      top: -15px;
      transform: translate(-50%, 0);
      border-left: 20px solid transparent;
      border-right: 20px solid transparent;
      border-bottom: 15px solid white;
    }

    form {
      width: 80%;
      margin: 20px auto;
      display: flex;
      flex-direction: column;
    }
  }
  .check::after {
    content: "Remember";
    position: relative;
    top: -5px;
    left: 20px;
  }
  button {
    height: 40px;
    border: none;
    background-color: crimson;
    border: 2px solid crimson;
    color: white;
    &:hover {
      color: crimson;
      background-color: white;
      border: 2px solid crimson;
    }
    p {
      margin: 0;
    }
  }
</style>

{#if visible}
  <div class="wrapper" on:mouseleave={modalClose}>
    <form>
      {#if login}
        <label for="email">Email address</label>
        <input name="email" />
        <label for="pass">Password</label>
        <input name="pass" />
        <input class="check" type="checkbox" name="check" />
        <button><p>LOGIN</p></button>
        <p>Forgot your password?</p>
      {/if}
      {#if register}
        <label for="email">Email address</label>
        <input name="email" />
        <label for="pass">Choose password</label>
        <input name="pass" />
        <label for="pass2">Confirm password</label>
        <input name="passw" />
        <button><p>Register Now</p></button>
      {/if}
    </form>
  </div>
{/if}
