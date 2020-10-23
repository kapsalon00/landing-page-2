<script>
  // your script goes here
</script>

<style lang="scss">
  .wrapper {
    background-color: white;
    .title {
      width: 100%;
      text-align: center;
      background-color: darkslategray;
      h1 {
        margin: 0;
        padding: 30px;
        font-size: 50px;
        color: white;
        font-weight: bold;
      }
    }
    .subtitle {
      width: 100%;
      text-align: center;
      background-color: crimson;
      h1 {
        margin: 0;
        padding: 30px;
        color: white;
      }
    }
  }
  .content {
    max-width: 960px;
    margin: 0 auto;
    h2 {
      margin-left: 10%;
    }
    p {
      width: 80%;
      margin: 20px auto;
    }
    button {
      margin-left: 10%;
      width: 200px;
      height: 40px;
      background-color: crimson;
      color: white;
      border-color: crimson;
      &:hover {
        transition: 0.3s;
        background-color: white;
        color: crimson;
      }
    }
    .image {
      width: 80%;
      height: 400px;
      margin: 20px auto;
      img {
        height: 100%;
        width: 100%;
        object-fit: cover;
        border-radius: 20px;
      }
    }
  }
</style>

<div class="wrapper">
  <div class="title">
    <h1>About Us</h1>
  </div>
  <div class="subtitle">
    <h1>Welcome to Our Website.</h1>
  </div>
  <div class="content">
    <h2>Lorem ipsum ipsum lore</h2>
    <div class="image"><img src="assets/details.jpg" alt="happy people" /></div>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua. Sit amet purus gravida
      quis blandit turpis cursus in. Ut lectus arcu bibendum at varius. Tellus
      molestie nunc non blandit massa enim. Diam sollicitudin tempor id eu nisl
      nunc. Quis viverra nibh cras pulvinar mattis nunc sed blandit libero. Ut
      placerat orci nulla pellentesque dignissim enim. Dui ut ornare lectus sit
      amet est placerat. Molestie at elementum eu facilisis. Non blandit massa
      enim nec dui nunc mattis. Pulvinar elementum integer enim neque volutpat
      ac tincidunt vitae. Parturient montes nascetur ridiculus mus mauris vitae.
      Et netus et malesuada fames ac turpis. Cras sed felis eget velit aliquet
      sagittis id. Tristique sollicitudin nibh sit amet commodo. Orci a
      scelerisque purus semper eget duis at tellus at.
    </p>
    <p>
      Eget egestas purus viverra accumsan in. Feugiat nisl pretium fusce id
      velit ut tortor pretium. Elementum integer enim neque volutpat ac. Cras
      sed felis eget velit aliquet. Aliquet porttitor lacus luctus accumsan
      tortor posuere. Ac tortor dignissim convallis aenean et tortor at risus.
      Aliquet risus feugiat in ante metus dictum. Sit amet nulla facilisi morbi
      tempus iaculis urna id volutpat. Quis commodo odio aenean sed. Pharetra
      vel turpis nunc eget. Tellus elementum sagittis vitae et leo duis ut diam
      quam. Ornare massa eget egestas purus.
    </p>
    <button>Read More</button>
  </div>
</div>
