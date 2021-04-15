<script lang="ts">
  import { Route } from "svelte-micro";
  import About from "./About.svelte";
  import Home from "./Home.svelte";
</script>

<Route>
  <nav>
    <a href="/">Home</a>
    <a href="/about">About</a>
  </nav>
  <Route path="/">
    <Home />
  </Route>
  <Route path="/about">
    <About />
  </Route>
  <Route fallback>
    <h1>Route not found :(</h1>
    <a href="/">Back to home</a>
  </Route>
</Route>
