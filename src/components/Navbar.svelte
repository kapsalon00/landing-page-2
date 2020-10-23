<script>
  import FaBuromobelexperte from "svelte-icons/fa/FaBuromobelexperte.svelte";
  import { createEventDispatcher } from "svelte";
  import Form from "./Form.svelte";
  import Modal from "./Modal.svelte";

  const dispatch = createEventDispatcher();

  let home = false;
  let about = false;
  let blog = false;

  const pageChange = (page) => {
    dispatch("pageChange", {
      page: page,
    });
  };

  let showLogin = false;
  let showRegister = false;

  const handleClose = () => {
    showLogin = false;
    showRegister = false;
  };

  let pageWidth;
  let showModal = false;
</script>

<style lang="scss">
  .wrapper {
    width: 100%;
    background-color: darkslategray;
  }
  .logo {
    color: white;
    width: 50px;
    height: 50px;
    &:hover {
      color: crimson;
      cursor: pointer;
    }
  }
  .navbar {
    padding: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  p {
    color: white;
  }
  .hamburger {
    .patty {
      width: 35px;
      height: 5px;
      background-color: black;
      margin: 6px 0;
    }
  }

  @media (min-width: 960px) {
    .wrapper {
      width: 100%;
      background-color: darkslategray;
    }
    .logo {
      color: white;
      width: 50px;
      height: 50px;
      &:hover {
        color: crimson;
        cursor: pointer;
      }
    }
    .navbar {
      padding: 20px;
      display: flex;
      justify-content: space-around;
      align-items: center;
    }
    p {
      color: white;
    }
    .links {
      display: flex;
      justify-content: space-around;
      align-items: center;
    }
    .link {
      margin: 0 10px;
      cursor: pointer;
      width: 80px;
      height: 40px;
      display: flex;
      justify-content: center;
      align-items: center;

      &:hover {
        background-color: crimson;
      }
    }
    .scene {
      margin: 0 10px;
      width: 80px;
      height: 40px;
      perspective: 1000px;
      cursor: pointer;
    }
    .cube {
      width: 100%;
      height: 100%;
      position: relative;
      transform-style: preserve-3d;
      transform: translateZ(-100px);
      transition: transform 0.2s;
    }

    .cube__face {
      display: flex;
      justify-content: center;
      align-items: center;
      position: absolute;
      width: 80px;
      height: 40px;
    }
    .cube__face--front {
      background-color: pink;
      transform: rotateY(0deg) translateZ(20px);
    }

    .cube__face--bottom {
      background-color: crimson;
      transform: rotateX(-90deg) translateZ(20px);
    }

    .cube.show-front {
      transform: translateZ(-20px) rotateY(0deg);
    }

    .cube.show-bottom {
      transform: translateZ(-20px) rotateX(90deg);
    }
  }
</style>

<svelte:window bind:outerWidth={pageWidth} />

<div class="wrapper">
  <div class="navbar">
    <div class="logo" on:click={() => pageChange('home')}>
      <FaBuromobelexperte />
    </div>
    {#if pageWidth < 960}
      {#if showModal}
        <Modal on:close={() => (showModal = false)}>
          <p
            style="color:black;"
            on:click={() => {
              pageChange('home');
              showModal = false;
            }}>
            HOME
          </p>
          <p
            style="color:black;"
            on:click={() => {
              pageChange('about');
              showModal = false;
            }}>
            ABOUT
          </p>
          <p
            style="color:black;"
            on:click={() => {
              pageChange('blog');
              showModal = false;
            }}>
            BLOG
          </p>
          <p style="color:black;">LOGIN</p>
          <p style="color:black;">SIGNUP</p>
        </Modal>
      {/if}
      <div
        class="hamburger"
        on:click={() => {
          showModal = true;
        }}>
        <div class="patty" />
        <div class="patty" />
        <div class="patty" />
      </div>
    {/if}
    {#if pageWidth >= 960}
      <div class="links">
        <div class="scene" on:click={() => pageChange('home')}>
          <div
            class="cube"
            on:mouseleave={() => (home = false)}
            on:mouseenter={() => (home = true)}
            class:show-front={home === false}
            class:show-bottom={home === true}>
            <div class="cube__face cube__face--front">
              <p>HOME</p>
            </div>
            <div class="cube__face cube__face--bottom">
              <p>HOME</p>
            </div>
          </div>
        </div>
        <div class="scene" on:click={() => pageChange('about')}>
          <div
            class="cube"
            on:mouseleave={() => (about = false)}
            on:mouseenter={() => (about = true)}
            class:show-front={about === false}
            class:show-bottom={about === true}>
            <div class="cube__face cube__face--front">
              <p>ABOUT</p>
            </div>
            <div class="cube__face cube__face--bottom">
              <p>ABOUT</p>
            </div>
          </div>
        </div>
        <div class="scene" on:click={() => pageChange('blog')}>
          <div
            class="cube"
            on:mouseleave={() => (blog = false)}
            on:mouseenter={() => (blog = true)}
            class:show-front={blog === false}
            class:show-bottom={blog === true}>
            <div class="cube__face cube__face--front">
              <p>BLOG</p>
            </div>
            <div class="cube__face cube__face--bottom">
              <p>BLOG</p>
            </div>
          </div>
        </div>
        <div
          class="link"
          on:click={() => {
            showLogin = true;
            showRegister = false;
          }}>
          <p>LOGIN</p>
          <Form on:modalClose={handleClose} visible={showLogin} login={true} />
        </div>
        <div
          class="link"
          on:click={() => {
            showRegister = true;
            showLogin = false;
          }}>
          <p>SIGNUP</p>
          <Form
            on:modalClose={handleClose}
            visible={showRegister}
            register={true} />
        </div>
      </div>
    {/if}
  </div>
</div>
