<script>
  import Team from "./Team.svelte";

  import Who from "./Who.svelte";
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
</style>

<div class="wrapper">
  <div class="title">
    <h1>About Us</h1>
  </div>
  <div class="subtitle">
    <h1>Welcome to Our Website.</h1>
  </div>
  <Who />
  <Team />
</div>
