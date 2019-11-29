<script>
  import Router, { link } from "svelte-spa-router";
  import active from "svelte-spa-router/active";

  import Home from "./Home.svelte";
  import Plans from "./Plans.svelte";
  import History from "./History.svelte";
  import Stash from "./Stash.svelte";
  import Referral from "./Referral.svelte";
  import Payment from "./Payment.svelte";

  const prefix = "/dashboard";
  const routes = {
    "/home": Home,
    "/plans": Plans,
    "/history": History,
    "/stash": Stash,
    "/payment": Payment
  };
</script>

<style>
  section {
    box-sizing: border-box;
    width: 100%;
    display: flex;
    flex: 0 1 auto;
    flex-direction: row;
    flex-wrap: wrap;
    background-color: #f4f7fa;
    height: 99vh;
    overflow: hidden;
  }
  .menu {
    flex-basis: 14%;
    width: 13%;
  }
 
  .sidenav-menu {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-top: 1px;
  }
  .logo-text {
    font-size: 1.4rem;
    font-weight: 500;
    color: #0066f5;
    text-decoration: none;
  }
  .greet_user {
    margin: 50px 0 30px;
    font-weight: 600;
    text-align: center;
    color: rgba(10, 46, 101, 0.2);
    font-size: 1.5rem;
  }
  .username {
    font-size: inherit;
    color: rgba(10, 46, 101, 0.5);
    cursor: pointer;
  }
  .sidenav-list {
    display: flex;
    flex-direction: column;
  }
  .item {
    font-weight: 500;
    font-size: 1rem;
    color: #0a2e65;
    opacity: 0.8;
    padding: 15px 25px;
    margin-bottom: 5px;
    width: 100%;
    transition-property: opacity, background-color;
    transition-duration: 0.2s;
    transition-timing-function: ease;
    background-color: transparent;
    border-radius: 8px;
  }
  :global(.item.active) {
    opacity: 1;
    color: #0066f5;
    background-color: rgba(0, 102, 245, 0.07);
  }
  .main {
    flex-basis: 86%;
    max-width: 86%;
    padding: 0;
  }
  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 30px;
  }
  .title {
    font-size: 0.8rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 1px;
    flex-basis: 100%;
    text-align: center;
  }
  .container {
    background-color: #fff;
    border-top-left-radius: 12px;
    box-shadow: -3px 3px 12px rgba(10, 46, 101, 0.03);
    padding: 20px 25px 0;
  }
  .scroll {
    height: 699px;
    overflow-y: auto;
    overflow-x: hidden;
    padding-bottom: 30px;
    scroll-behavior: smooth;
  }

   @media screen and (max-width:600px){
    .menu{
      display:none;
    }
     .main {
    flex-basis: 100%;
    max-width: 100%;
    padding: 0;
  }
  }
</style>

<section>
  <div class="menu">
    <div class="sidenav">
      <div class="sidenav-menu">
        <p>
          <a href="/">
            <span class="logo-text">clearIT</span>
          </a>
        </p>
        <h4 class="greet_user">
          Howdy
          <span class="username">Peter</span>
        </h4>
        <div class="sidenav-list">

          <a
            href="/dashboard/home"
            use:link
            use:active={{ path: '/dashboard/home', className: 'active' }}
            class="item">
            Home
          </a>

          <a
            href="/dashboard/plans"
            use:link
            use:active={{ path: '/dashboard/plans', className: 'active' }}
            class="item">
            Plans
          </a>

          <a
            href="/dashboard/history"
            use:link
            use:active={{ path: '/dashboard/history', className: 'active' }}
            class="item">
            History
          </a>

          <a
            href="/dashboard/stash"
            use:link
            use:active={{ path: '/dashboard/stash', className: 'active' }}
            class="item">
            Stash
          </a>
          <a
            href="/dashboard/payment"
            use:link
            use:active={{ path: '/dashboard/payment', className: 'active' }}
            class="item">
            Payment
          </a>

          <div class="item">LogOut</div>
        </div>
      </div>
    </div>
  </div>
  <div class="main">
    <div class="navbar">
      <span class="title">Account Overview</span>
    </div>
    <div class="container">
      <div class="scroll">
        <Router {routes} {prefix} />
      </div>
    </div>
  </div>
</section>
