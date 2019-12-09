<script>
  //BUTT
  // <svg
  //           xmlns="http://www.w3.org/2000/svg"
  //           viewBox="0 0 200 100"
  //           preserveAspectRatio="none">
  //           <circle fill="white" cx="0" cy="100" r="100" />
  //           <circle fill="white" cx="200" cy="100" r="100" />
  //         </svg>

  //Curved
  //  background-image: linear-gradient(#ff9d2f, #ff6126);
  // border-bottom-left-radius: 50% 20%;
  // border-bottom-right-radius: 50% 20%;

  //Skew
  // content: "";
  //   position: absolute;
  //   z-index: -1;
  //   width: 100%;
  //   height: 180%;
  //   top: 0;
  //   -webkit-transform: skewY(-12deg);
  //   transform: skewY(-12deg);
  //   background: #f6f9fc;

  import jQuery from "jquery";
  import { onMount } from "svelte";

  let button;
  let span;
  let active = true;
  let closed = false;
  let modal = true;
  onMount(() => {
    button = document.getElementById("hamburger-menu");
    span = document.getElementById("span");
    button.onclick = function() {
      span.classList.toggle("hamburger-menu-button-close");
    };
    jQuery("#hamburger-menu").on("click", toggleOnClass);

    function toggleOnClass(event) {
      var toggleElementId = "#" + jQuery(this).data("toggle"),
        element = jQuery(toggleElementId);

      element.toggleClass("on");
    }
  });

  // close hamburger menu after click a
  // $( '.menu li a' ).on("click", function(){
  //   $('#hamburger-menu').click();
  // });
</script>

<style type="text/scss">
  .modal {
    display: none;
  }
  .overlay{
    position:fixed;
    z-index: 9;
    top:0;
    right:0;
    height:100%;
    width:100%;
    background:rgba(0,0,0,0.8);
  }
  .nav-mo {
    position: fixed;
    top: 1rem;
    right: 5%;
    height: 70vh;
    padding: 1rem;
    width: 90%;
    background: white;
    z-index: 99999999999999999999999;
    border-radius: 5px;
  }
  header {
    padding: 3% 5%;
    padding-bottom: 10%;
    background-size: cover;
    background-attachment: fixed;
    position: relative;
    // box-shadow: inset 0 0 0 2000px #000000b3;
    color: white;
    overflow: hidden;
    margin:0 auto;
    margin-bottom: 23rem;
    background-color: #f4f7fa;
    height: 50rem;
    @media screen and (max-width:600px){
      height: 40rem;
    }
    .bg {
      width: 100%;
      height: 120%;
      position: absolute;
      top: 0;
      left: 0;
      transform: skewY(-47deg);
      overflow: hidden;
      transform-origin: 0;
      border-bottom: 20px solid #8abdf3;
      // background: linear-gradient(150deg,#53f 15%,#05d5ff 70%,#a6ffcb 94%);
      background: url(images/container.jpg);
      background-size: cover;
      background-repeat: no-repeat;
      background-attachment: fixed;
      box-shadow: inset 0 0 0 2000px rgba(0, 0, 0, 0.5);
      // background-position: right 45px bottom 20px;
        @media screen and (max-width:600px){
      transform: unset;
    }
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
    z-index: 999999;
    max-width:1600px;


    .logo {
      font-size: 2.5rem;
      z-index: 5;
    }
    a {
      text-decoration: none;
      cursor: pointer;
      display: inline-block;
      font-size: 15px;
      min-height: 36px;
      color: var(--accent-color);
      border-radius: 5px;
      padding: 5px 0;
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
      background: var(--accent-color);
      border: none;
      color: white;
    }
  }

  .hamburg {
    display: none;
    @media screen and (max-width: 600px) {
      display: block;
    }
  }
  .hamburger-menu-button {
    width: 30px;
    height: 30px;
    padding: 3px;
    display: block;
    position: relative;
    z-index: 5;
    background: #2980b9;
    border: 1px solid white;
    box-sizing: content-box;
    border-radius: 50%;
    text-indent: 100%;
    color: transparent;
    white-space: nowrap;
    cursor: pointer;
    overflow: hidden;
  }
  .active {
    top: 50%;
    margin-top: -1px;
    left: 50%;
    margin-left: -12px;
  }
  .active,
  .active::before,
  .active::after {
    position: absolute;
    width: 24px;
    height: 2px;
    background: #fff;
    border-radius: 4px;
    -webkit-transition: all 0.3s;
    transition: all 0.3s;
  }
  .active::before,
  .active::after {
    left: 0;
    content: "";
  }
  .active::before {
    top: 6px;
  }
  .active::after {
    bottom: 6px;
  }
  .hamburger-menu-button-close {
    background: transparent;
    -webkit-transform: rotate(180deg);
    transform: rotate(180deg);
  }
  .hamburger-menu-button-close::before {
    -webkit-transform: translateY(-6px) rotate(45deg);
    transform: translateY(-6px) rotate(45deg);
  }
  .hamburger-menu-button-close::after {
    -webkit-transform: translateY(6px) rotate(-45deg);
    transform: translateY(6px) rotate(-45deg);
  }
  section {
    width: 55%;
    position: absolute;
    top: 40%;
    right: 0;
    max-width:1600px;
    @media screen and (max-width: 600px) {
    top:40%;
    right:5%;
    width:90%;
    }
    h1 {
      font-size: 3.5rem;
      opacity: 0;
      color: var(--accent-color);
      width: 100%;
      max-width:700px;
      margin-top: 200px;
      animation: 3s slidefade 0.3s forwards;
      @media screen and (max-width: 1200px) {
        font-size: 3rem;
        width: 90%;
      }
      @media screen and (max-width: 600px) {
        font-size: 2.5rem;
        width: 100%;
        color:white;
      }
    }
    @keyframes slidefade {
      100% {
        opacity: 1;
        margin-top: 0;
      }
    }

    form{
      display: flex;
    max-width: 700px;
    justify-content: space-between;
    background: #fff;
    padding: .5rem;
    box-shadow: 0 12px 50px 0 rgba(0,0,0,.15);
    border-radius: 5px;
      @media screen and (max-width:600px){
      flex-direction: column;
      width:100%;
      margin:0 auto;
    }
    }

    .form-group{
      margin-bottom: 0;
    width: 100%;
    }
    input{
          padding: .5rem .75rem;
    width: 515px;
    border:none;
    line-height:3;
      @media screen and (max-width:600px){
    width:100%;
    }
    &:focus{
      outline:none;
    }
    }
    button{
      font-weight: 400;
    padding: .7rem 2rem;
    border-radius: 5px;
      background: var(--accent-color);
    color: #fff;
    border: none;
    width:180px;
    max-width:250px;
    cursor:pointer;
      @media screen and (max-width:600px){
      width:100%;
      max-width:unset;
         }
    }
  }
  @media screen and (max-width: 600px) {
    .nav-items {
      display: none;
    }
  }
</style>

<div class:modal>
<div class="overlay"></div>
 <div class="nav-mo">
   hello
 </div>
</div>
<header>
  <div class="bg">
    <!-- <img src="images/container.jpg" class="bgi" /> -->
  </div>
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
        <a href="/">Contact Us</a>
      </div>
      <div class="auth">
        <a href="/">About Us</a>
      </div>
      <div class="auth">
        <a href="#/auth/login" class="register">Sign In</a>
      </div>
    </div>
    <div class="hamburg">
      <button
        id="hamburger-menu"
        data-toggle="ham-navigation"
        class="hamburger-menu-button">
        <span
          class:active={'active'}
          class:closed={'closed'}
          id="span"
          on:click={() => {
            modal = !modal;
          }}>
          Menu
        </span>
      </button>
    </div>
  </nav>
  <section>
    <h1>Clear cargo transparently and efficiently in Africa</h1>
    <div class="get-started">
    <form>
      <div class="form-group" >
      <input type="email" placeholder="Enter your email"/>
      </div>
      <button>Get Started</button>
    </form>
    </div>
  </section>

</header>
