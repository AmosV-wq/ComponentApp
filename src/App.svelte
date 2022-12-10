<script>
  import Home from "./pages/Home.svelte";
  import { Router, Route } from "svelte-navigator";
  import TopBars from "./pages/TopBars.svelte";
  import Buttons from "./pages/Buttons.svelte";
  import Cards from "./pages/Cards.svelte";
  import Loader from "./pages/Loaders.svelte";
  import Split from "./pages/Split.svelte";
  import Paralax from "./pages/Paralax.svelte";
</script>

<main>
  <Router primary={false}>
    <Route path="/">
      <Home />
    </Route>
    <Route path="topBars">
      <TopBars />
    </Route>
    <Route path="buttons">
      <Buttons />
    </Route>
    <Route path="cards">
      <Cards />
    </Route>
    <Route path="loader">
      <Loader />
    </Route>
    <Route path="split">
      <Split />
    </Route>
    <Route path="paralax">
      <Paralax />
    </Route>
  </Router>
</main>
