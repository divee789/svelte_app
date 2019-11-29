<script>

</script>

<style type="text/scss">
  header {
    padding: 3% 5%;
    background: url(images/container.jpg);
    background-size: cover;
    background-attachment: fixed;
    box-shadow: inset 0 0 0 2000px rgba(0, 0, 0, 0.7);
    color: white;
    a {
      text-decoration: none;
      cursor: pointer;
      display: inline-block;
      font-size: 15px;
      min-height: 36px;
      color: white;
      border-radius: 5px;
      line-height: 36px;
      padding-left: 1.2em;
      padding-right: 1.2em;
      position: relative;
      transition: all 0.3s;
    }
  }
  nav {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    font-family: Sailec;
    align-items: center;
    transition: all 0.5s linear;
    .logo {
      font-size: 1.5rem;
    }
    a {
      text-decoration: none;
      cursor: pointer;
      display: inline-block;
      font-size: 15px;
      min-height: 36px;
      color: white;
      border-radius: 5px;
      line-height: 36px;
      padding-left: 1.7em;
      padding-right: 1.7em;
      position: relative;
      transition: all 0.3s;
    }
    .auth {
      display: inline-block;
    }
    .sign-in {
      background-color: transparent;
      border: 1px solid var(--accent-color);
      margin-right: 20px;
    }
    .register {
      background-image: var(--background);
      border: none;
    }
  }
  section {
    padding: 17% 0;
    padding-bottom: 8%;
    max-width: 1300px;
    @media screen and (max-width: 600px) {
      padding: 50% 0;
      height: 70vh;
    }
    h1 {
      font-size: 4rem;
      opacity: 0;
      width: 70%;
      margin-top: 200px;
      animation: 3s slidefade 0.3s forwards;
      @media screen and (max-width: 1200px) {
        font-size: 3rem;
        width: 90%;
      }
      @media screen and (max-width: 600px) {
        font-size: 2rem;
        width: 100%;
        text-align: center;
      }
    }
    @keyframes slidefade {
      100% {
        opacity: 1;
        margin-top: 0;
      }
    }
    .input {
      width: 50%;
      margin-bottom: 1rem;
      @media screen and (max-width: 600px) {
        width: 100%;
      }
      input {
        width: 100%;
        padding: 1.2rem 10px;
        border-radius: 5px;
        border: none;
        font-size: 1.1rem;
        text-align: center;
        background: rgba(255, 255, 255, 0.08);
        border: 1.2px solid purple;
        @media screen and (max-width: 600px) {
          font-size: 0.9rem;
        }
        &::placeholder {
          color: purple;
        }
      }
    }
    .button {
      background: var(--background);
      width: 50%;
      padding: 0.3rem 0;
      font-size: 13px;
      display: flex;
      cursor: pointer;
      justify-content: center;
      @media screen and (max-width: 600px) {
        width: 100%;
      }
    }
  }
  @media screen and (max-width: 600px) {
    .nav-items {
      display: none;
    }
  }
</style>

<header>
  <nav>
    <div class="logo">ClearIT</div>
    <div class="nav-items">
      <div class="auth">
        <a href="/">Solutions</a>
      </div>
      <div class="auth">
        <a href="/">Blog</a>
      </div>
      <div class="auth">
        <a href="/">About Us</a>
      </div>
      <div class="auth">
        <a href="#/auth/login" class="register">Sign In</a>
      </div>
    </div>
  </nav>
  <section>
    <h1>Clear cargo transparently and efficiently in Africa</h1>
    <div class="input">
      <input type="text" placeholder="TRACKING ID" />
    </div>
    <div class="button">
      <a href="#/auth/register">GET STARTED</a>
    </div>
  </section>

</header>
