<script>
  // your script goes here
</script>

<style lang="scss">
  main {
    margin: 0 auto;
    background-color: white;
    text-align: center;
    padding: 30px;
  }
  .wrapper {
    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: center;

    .image {
      margin: 0 20px;

      img {
        width: 200px;
        height: 200px;
        object-fit: cover;
        border-radius: 50%;
      }
    }
  }
  @media (min-width: 960px) {
    main {
      max-width: 1160px;
      margin: 0 auto;
      background-color: white;
      text-align: center;
      padding: 30px;
    }
    .wrapper {
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: center;

      .image {
        margin: 0 20px;

        img {
          width: 200px;
          height: 200px;
          object-fit: cover;
          border-radius: 50%;
        }
      }
    }
  }
</style>

<main>
  <h1>The Team</h1>
  <div class="wrapper">
    <div class="image">
      <img src="assets/team1.jpg" alt="pic" />
      <h1>Kelly Random</h1>
      <h3>CEO</h3>
      <p>
        Lorem ipsum is simply dummy text of the printing and typesetting
        industry.Lorem ipsum has been
      </p>
    </div>
    <div class="image">
      <img src="assets/team2.jpg" alt="pic" />

      <h1>Marque Random</h1>
      <h3>Creative Director</h3>
      <p>
        Lorem ipsum is simply dummy text of the printing and typesetting
        industry.Lorem ipsum has been
      </p>
    </div>
    <div class="image">
      <img src="assets/team3.jpg" alt="pic" />

      <h1>Mona Random</h1>
      <h3>CTO</h3>
      <p>
        Lorem ipsum is simply dummy text of the printing and typesetting
        industry.Lorem ipsum has been
      </p>
    </div>
  </div>
</main>
