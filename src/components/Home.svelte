<script>
  import WiAlien from "svelte-icons/wi/WiAlien.svelte";
  import WiMeteor from "svelte-icons/wi/WiMeteor.svelte";
  import WiLightning from "svelte-icons/wi/WiLightning.svelte";
  import FaCarrot from "svelte-icons/fa/FaCarrot.svelte";
  import { createEventDispatcher } from "svelte";

  const dispatch = createEventDispatcher();

  const pageChange = (page) => {
    dispatch("pageChange", {
      page: page,
    });
  };
</script>

<style lang="scss">
  .wrapper {
    background-color: darkslategray;
  }
  main {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin: 0 auto;
    padding: 10px;
    h1,
    p {
      text-align: center;
      color: white;
    }
    .left,
    .right {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }
    .actions {
      width: 100%;
      display: flex;
      flex-direction: column;
      justify-content: space-around;
      align-items: center;
      button {
        width: 150px;
        height: 40px;
        color: white;
      }
      .signup {
        border: none;
        background-color: crimson;
        &:hover {
          background-color: darkslategray;
          border: 2px solid crimson;
          color: crimson;
        }
      }
      .learnmore {
        border: none;
        background-color: darkslategray;
        border: 2px solid white;
        &:hover {
          color: crimson;
          border: 2px solid crimson;
        }
      }
    }
  }

  .smartphone {
    position: relative;
    width: 180px;
    height: 320px;
    margin: auto;
    border: 16px black solid;
    border-top-width: 30px;
    border-bottom-width: 30px;
    border-radius: 18px;
  }

  /* The horizontal line on the top of the device */
  .smartphone:before {
    content: "";
    display: block;
    width: 60px;
    height: 5px;
    position: absolute;
    top: -15px;
    left: 50%;
    transform: translate(-50%, -50%);
    background: #333;
    border-radius: 10px;
  }

  /* The circle on the bottom of the device */
  .smartphone:after {
    content: "";
    display: block;
    width: 15px;
    height: 15px;
    position: absolute;
    left: 50%;
    bottom: -30px;
    transform: translate(-50%, -50%);
    background: #333;
    border-radius: 50%;
  }

  /* The screen (or content) of the device */
  .smartphone .content {
    width: 180px;
    height: 320px;
    background: #666666;
    .on-screen {
      width: 80px;
      height: 80px;
      color: orange;
      margin: 0px auto;
      padding-top: 60px;
    }
  }
  .iswrapper {
    background-color: #750b20;
  }
  .icons-section {
    max-width: 1260px;
    margin: 0 auto;
    background-color: #750b20;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    .card {
      padding: 30px 0;
      width: 300px;
      text-align: center;
      h2,
      p {
        color: white;
      }
      .icon {
        color: white;
        width: 80px;
        margin: 0 auto;
      }
    }
  }

  @media (min-width: 960px) {
    .wrapper {
      margin: 0 auto;
    }
    main {
      max-width: 1260px;
      margin: 0 auto;
      padding: 100px;
      display: flex;
      flex-direction: row;
      h1,
      p {
        color: white;
      }
      .left,
      .right {
        width: 50%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
      }
      .actions {
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        align-items: center;
        button {
          width: 150px;
          height: 40px;
          color: white;
        }
        .signup {
          border: none;
          background-color: crimson;
          &:hover {
            background-color: darkslategray;
            border: 2px solid crimson;
            color: crimson;
          }
        }
        .learnmore {
          border: none;
          background-color: darkslategray;
          border: 2px solid white;
          &:hover {
            color: crimson;
            border: 2px solid crimson;
          }
        }
      }
    }
    .iswrapper {
      background-color: #750b20;
    }
    .icons-section {
      max-width: 1260px;
      margin: 0 auto;
      background-color: #750b20;
      display: flex;
      flex-direction: row;
      justify-content: space-around;
      align-items: center;
      .card {
        padding: 30px 0;
        width: 300px;
        text-align: center;
        h2,
        p {
          color: white;
        }
        .icon {
          color: white;
          width: 80px;
          margin: 0 auto;
        }
      }
    }
    .right {
      .smartphone {
        position: relative;
        width: 180px;
        height: 320px;
        margin: auto;
        border: 16px black solid;
        border-top-width: 30px;
        border-bottom-width: 30px;
        border-radius: 18px;
      }

      /* The horizontal line on the top of the device */
      .smartphone:before {
        content: "";
        display: block;
        width: 60px;
        height: 5px;
        position: absolute;
        top: -15px;
        left: 50%;
        transform: translate(-50%, -50%);
        background: #333;
        border-radius: 10px;
      }

      /* The circle on the bottom of the device */
      .smartphone:after {
        content: "";
        display: block;
        width: 15px;
        height: 15px;
        position: absolute;
        left: 50%;
        bottom: -30px;
        transform: translate(-50%, -50%);
        background: #333;
        border-radius: 50%;
      }

      /* The screen (or content) of the device */
      .smartphone .content {
        width: 180px;
        height: 320px;
        background: #666666;
        .on-screen {
          width: 80px;
          height: 80px;
          color: orange;
          margin: 0px auto;
          padding-top: 60px;
        }
      }
    }
  }
</style>

<div class="wrapper">
  <main>
    <div class="left">
      <h1>Challenges are meant to be met and overcome</h1>
      <p>
        [Company name] is mobile solution to Lorem ipsum dolor sit amet,
        consectetur elit, sed do eiusmod tempor incididunt ut labore et dolore
        magna aliqua.
      </p>
      <div class="actions">
        <button class="signup">SIGN UP</button><button
          on:click={() => pageChange('details')}
          class="learnmore">LEARN MORE &gt;</button>
      </div>
    </div>
    <div class="right">
      <div class="smartphone">
        <div class="content">
          <div class="on-screen">
            <FaCarrot />
            <h1>Noice</h1>
          </div>
        </div>
      </div>
    </div>
  </main>
</div>

<div class="iswrapper">
  <div class="icons-section">
    <div class="card">
      <div class="icon">
        <WiAlien />
      </div>
      <h2>Lorem ipsum dolor sit amet, consectetur adipiscing</h2>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua.
      </p>
    </div>
    <div class="card">
      <div class="icon">
        <WiMeteor />
      </div>
      <h2>Lorem ipsum dolor sit amet, consectetur adipiscing</h2>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua.
      </p>
    </div>
    <div class="card">
      <div class="icon">
        <WiLightning />
      </div>
      <h2>Lorem ipsum dolor sit amet, consectetur adipiscing</h2>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua.
      </p>
    </div>
  </div>
</div>
