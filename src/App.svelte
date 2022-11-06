<script>
  import Home from "./pages/Home.svelte";
  import { Router, Route } from "svelte-navigator";
  import TopBars from "./pages/TopBars.svelte";
  import Buttons from "./pages/Buttons.svelte";
  import Cards from "./pages/Cards.svelte";
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
  </Router>
</main>
