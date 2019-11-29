<script>
  import Router from "svelte-spa-router";
  import HomePage from "./HomePage.svelte";
  import Login from "./Login.svelte";
  import SignUp from "./SignUp.svelte";
  import Dashboard from "./components/Dashboard/index.svelte";

  const routes = {
    // Exact path
    "/": HomePage,

    "/auth/login": Login,

    "/auth/register": SignUp,
    '/dashboard':Dashboard,
    '/dashboard/*':Dashboard,

    // Catch-all
    // This is optional, but if present it must be the last
    "*": HomePage
  };
</script>

<style>

</style>

<div>
  <Router {routes} />
</div>
