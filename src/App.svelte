<script>
  import Navbar from "./components/Navbar.svelte";
  import Home from "./components/Home.svelte";
  import About from "./components/About.svelte";
  import Blog from "./components/Blog.svelte";
  import Footer from "./components/Footer.svelte";
  import Details from "./components/Details.svelte";

  let page = "home";
</script>

<style lang="scss">
  /* your styles go here */
</style>

<main>
  <Navbar on:pageChange={(event) => (page = event.detail.page)} />

  {#if page === 'home'}
    <Home on:pageChange={(event) => (page = event.detail.page)} />
  {/if}
  {#if page === 'about'}
    <About />
  {/if}
  {#if page === 'blog'}
    <Blog />
  {/if}
  {#if page === 'details'}
    <Details />
  {/if}

  <Footer />
</main>
