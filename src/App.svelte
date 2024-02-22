<script lang="ts">
  import App2 from "./App2.svelte";
  import { Router, Route } from "svelte-routing";
  import RouteTest from "./RouteTest.svelte";
</script>

<Router url="">
  <Route path="/">
    <App2 />
  </Route>
  <Route path="/test/:id" let:params>
    <RouteTest id={params.id} />
  </Route>
  <Route path="*">
    <div>notfound</div>
  </Route>
</Router>
