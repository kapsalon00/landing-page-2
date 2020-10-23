<script>
  // your script goes here
</script>

<style lang="scss">
  main {
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 10px;
  }
  .left {
    margin: 0 auto;
    .picture {
      max-width: 400px;
      max-height: 250px;
      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    }
  }
  .right {
    margin: 0 auto;
    .slider-container {
      .text-container {
        display: flex;
        justify-content: space-between;
        h2 {
          color: grey;
        }
      }
      .outer-slider {
        border-radius: 20px;
        width: 100%;
        height: 10px;
        background-color: lightgrey;
        @keyframes Animation {
          100% {
            background-position: 10px 0px;
          }
        }

        .inner-slider {
          border-radius: 20px;
          height: 100%;
          background: linear-gradient(
            -45deg,
            rgba(255, 255, 255, 0.5) 25%,
            transparent 25%,
            transparent 50%,
            rgba(255, 255, 255, 0.5) 50%,
            rgba(255, 255, 255, 0.5) 75%,
            transparent 75%,
            transparent
          );
          background-color: crimson;
          background-size: 10px;
          animation: Animation 0.5s linear infinite;
        }
      }
    }
  }
  @media (min-width: 960px) {
    main {
      max-width: 1160px;
      margin: 0 auto;
      display: flex;
      flex-direction: row;
      justify-content: center;
      align-items: center;
      padding: 30px;
    }
    .left {
      margin: 0 auto;
      .picture {
        width: 400px;
        height: 250px;
        img {
          width: 100%;
          height: 100%;
          object-fit: cover;
        }
      }
    }
    .right {
      margin: 0 auto;
      .slider-container {
        .text-container {
          display: flex;
          justify-content: space-between;
          h2 {
            color: grey;
          }
        }
        .outer-slider {
          border-radius: 20px;
          width: 100%;
          height: 10px;
          background-color: lightgrey;
          @keyframes Animation {
            100% {
              background-position: 10px 0px;
            }
          }

          .inner-slider {
            border-radius: 20px;
            height: 100%;
            background: linear-gradient(
              -45deg,
              rgba(255, 255, 255, 0.5) 25%,
              transparent 25%,
              transparent 50%,
              rgba(255, 255, 255, 0.5) 50%,
              rgba(255, 255, 255, 0.5) 75%,
              transparent 75%,
              transparent
            );
            background-color: crimson;
            background-size: 10px;
            animation: Animation 0.5s linear infinite;
          }
        }
      }
    }
  }
</style>

<main>
  <div class="left">
    <h1>Who we are?</h1>
    <div class="picture">
      <img src="assets/sunset.jpg" alt="girl looking at sunset" />
    </div>
  </div>
  <div class="right">
    <h1>Our best skills</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do</p>
    <div class="slider-container">
      <div class="text-container">
        <h2>Web & Ui design</h2>
        <h2>80%</h2>
      </div>
      <div class="outer-slider">
        <div class="inner-slider" style="width:80%" />
      </div>
    </div>
    <div class="slider-container">
      <div class="text-container">
        <h2>Something</h2>
        <h2>90%</h2>
      </div>
      <div class="outer-slider">
        <div class="inner-slider" style="width:90%" />
      </div>
    </div>
    <div class="slider-container">
      <div class="text-container">
        <h2>iOs Development</h2>
        <h2>50%</h2>
      </div>
      <div class="outer-slider">
        <div class="inner-slider" style="width:50%" />
      </div>
    </div>
    <div class="slider-container">
      <div class="text-container">
        <h2>Design</h2>
        <h2>60%</h2>
      </div>
      <div class="outer-slider">
        <div class="inner-slider" style="width:60%" />
      </div>
    </div>
  </div>
</main>
