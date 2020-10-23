<script>
  import { createEventDispatcher, onDestroy } from "svelte";
  const dispatch = createEventDispatcher();
  const close = () => dispatch("close");
  let modal;
  const previously_focused =
    typeof document !== "undefined" && document.activeElement;
  if (previously_focused) {
    onDestroy(() => {
      previously_focused.focus();
    });
  }
</script>

<style>
  .modal-background {
    z-index: 2;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.3);
  }
  .modal {
    z-index: 3;
    position: absolute;
    left: 50%;
    top: 50%;
    width: calc(100vw - 4em);
    max-width: 32em;
    max-height: calc(100vh - 4em);
    overflow: auto;
    transform: translate(-50%, -50%);
    padding: 1em;
    border-radius: 0.2em;
    background: white;
  }
  .nav {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
</style>

<div class="modal-background" on:click={close} />

<div class="modal" bind:this={modal}>
  <div class="nav">
    <slot />
  </div>
</div>
