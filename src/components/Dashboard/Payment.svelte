<script>
import {fade} from 'svelte/transition'
</script>

<style>
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
</style>

<section>
  <div class="navbar">
    <span class="title">Banks and Cards</span>
  </div>
  <div class="container">
    <div class="scroll">
      <div in:fade={{ duration: 500 }}>my payments</div>
    </div>
  </div>
</section>