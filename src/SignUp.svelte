<script>
  import { link } from "svelte-spa-router";
</script>

<style>
  .section {
    background-color: #f4f7fa;
    padding-bottom: 1rem;
    box-sizing: border-box;
 }
  .grid {
    box-sizing: border-box;
    width: 100%;
    display: flex;
    flex: 0 1 auto;
    flex-direction: row;
    flex-wrap: wrap;
  }
  .auth-container {
    margin: 0 auto;
    max-width: 1300px;
    padding: 0 60px;
    width: 100%;
    padding-top: 80px;
  }
  .body {
    margin-bottom: 7rem;
  }
  .nav-content {
    box-sizing: border-box;
    flex-basis: 100%;
    max-width: 100%;
    padding: 0;
    font-size: 18px;
  }
  .auth-title {
    box-sizing: border-box;
    flex-basis: 50%;
    max-width: 50%;
    padding: 0;
  }
  h3 {
    font-weight: 700;
    font-size: 3.5rem;
    color: #0a2e65;
    margin: 0;
    margin-bottom: 3px;
  }
  h4 {
    font-weight: 700;
    font-size: 3rem;
    color: rgba(10, 46, 101, 0.3) !important;
    margin-top: 0;
  }
  .auth-box {
    border: 1px solid rgba(0, 102, 245, 0.15);
    background-color: #fff;
    padding: 40px 40px 30px;
    min-height: 200px;
    position: relative;
    overflow: hidden;
    box-shadow: 1px 15px 18px rgba(0, 0, 0, 0.03);
    border-radius: 6px;
  }
  .auth-footer {
    box-sizing: border-box;
    justify-content: space-between;
    margin-top: 30px;
  }
  .input-field {
    position: relative;
    margin-bottom: 30px;
  }
  .flex{
      display:flex;
      flex-direction: row;
      justify-content: space-between;
  }
  .flex-item{
      width: 48%;
  }
  .input-footer {
    box-sizing: border-box;
    align-items: center;
  }
  input {
    appearance: none;
    transition: border-color 0.3s ease-in, color 1s linear;
    width: 100%;
    display: block;
    height: 56px;
    background-color: transparent;
    border-radius: 4px;
    outline: none;
    color: #0a2e65;
    border: 1px solid rgba(10, 46, 101, 0.1);
    font-family: Sailec, -apple-system, BlinkMacSystemFont, Segoe UI, Roboto,
      Oxygen-Sans, Ubuntu, Cantarell, Helvetica Neue, sans-serif;
    font-size: 0.95rem;
    padding-bottom: 10px;
    padding-top: 10px;
    padding-left: 20px;
  }
  input:focus{
      border:1px solid #0066f5;
  }

  .input-helper {
    font-size: 0.7rem;
    position: absolute;
    opacity: 1;
    background-color: #fff;
    padding-left: 8px;
    padding-right: 8px;
    top: -7px;
    color: rgba(10, 46, 101, 0.5);
    transition: color 0.3s ease;
    left: 12px;
  }
  .forgot{
    margin-top:1rem;
    font-size: 12px;
  }
  input:focus > .input-helper {
    opacity: 1;
  }
  .auth-btn {
    display: flex;
    justify-content: flex-end;
  }
  .signin-text {
    color: rgba(10, 46, 101, 0.6) !important;
    font-size: 0.8rem;
  }
  .a {
    color: #0066f5;
    font-size: inherit;
    font-weight: bold;
  }
  button {
    outline: 0;
    background-color: #0066f5;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    display: inline-block;
    font-size: 0.95rem;
    min-height: 42px;
    color: #fff;
    line-height: 42px;
    position: relative;
    text-decoration: none;
    padding: 0 1.8em 2.5px;
    transition-duration: 0.3s;
    font-weight: 600;
    text-transform: capitalize;
    transition-property: background-color, opacity, color, transform, box-shadow;
    transition-timing-function: ease-in-out;
    user-select: none;
    transform-style: preserve-3d;
    will-change: background-color, opacity, color, transform, box-shadow;
    box-shadow: 0 2px 4px 0 rgba(10, 46, 101, 0.08);
  }
  .auth-footer {
    justify-content: space-between;
    margin-top: 30px;
  }
  .u {
    color: rgba(10, 46, 101, 0.3) !important;
    font-size: 0.8rem;
    font-weight: 600;
  }
    @media screen and (max-width: 800px) {
    .section {
      height: 100%;
      padding-bottom: 10%;
    }
    .grid{
        flex-direction: column;
      }
      .auth-title{
        flex-basis: 100%;
        max-width:100%;
        margin-bottom: 20px;
      }
      .auth-container{
        padding:0 30px;
      }
      h3{
        font-size: 2.5rem;
      }
      h4{
        font-size: 2rem;
      }
  }
</style>

<section class="section">
  <section class="auth-container">
    <div class="body grid">
      <div class="nav-content">
        <a href="/"><span class="a">ClearIT</span></a>
      </div>
    </div>
    <div class="body grid">
      <div class="auth-title">
        <h3>Create an account</h3>
        <h4>in ~5 minutes</h4>
      </div>
      <div class="auth-title">
        <div class="auth-box">
          <form>
             <div class="input-field flex">
              <div class="flex-item">
                <input type="text" placeholder="First Name" />
              <span class="input-helper">First Name</span>
              </div>
              <div class="flex-item">
                <input type="text" placeholder="Last Name" />
              <span class="input-helper">Last Name</span>
              </div>
            </div>
           <div class="input-field">
              <input type="text" placeholder="Phone number" />
              <span class="input-helper">Phone number</span>
            </div>
            <div class="input-field">
              <input type="email" placeholder="Email Address" />
              <span class="input-helper">Email Address</span>
            </div>
            <div class="input-field">
              <input type="password" placeholder="Password" />
              <span class="input-helper">Password</span>
                <div class="forgot"><a href="/"><span class="a">Got invite code?</span></a></div>
            </div>
          
            <div class="input-footer grid">
              <div class="create auth-title">
                <span class="signin-text">
                  Got an account?
                  <a href="#/auth/login"><span class="a">Sign in</span></a>
                </span>
              </div>
              <div class="auth-btn auth-title">
                <button>Continue</button>
              </div>
            </div>
          </form>
        </div>
        <div class="auth-footer grid">
          <div class="signin-text">
            Trouble signing in?
            <a href="/"><span class="a">Contact Support</span></a>
          </div>
          <div>
            <span class="u">Privacy |</span>
            <span class="u">Terms</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</section>
