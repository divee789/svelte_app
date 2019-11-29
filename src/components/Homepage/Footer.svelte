<script>
  import FooterContent from "./FooterContent.svelte";
</script>

<style>
  .container {
    /* margin: 0 auto; */
    position: relative;
    padding: 5rem 50px;
    width: 100%;
    background:#eaf4ff;
    color:black;
  }
  .get-started{
    width:70%;
    margin:0 auto;
    margin-bottom:-39px;
    padding:2.3rem;
    background: var(--accent-color);
    color:#fff;
    font-weight:600;
    border-radius:10px;
    box-shadow: 4px 12px 20px 0 rgba(0,0,0,.3);
    text-align:center;
    z-index: 99999;
  }
  h2{
    font-size: 2.5rem;
  }
  p{
    font-size:.93rem;
    margin-bottom:2.1rem;
    color: hsla(0,0%,100%,.548);
  }
  .button{
    background: #fff;
    color:#151027;
    border-radius:11px;
  }
  footer{
    z-index: -1;
  }
   @media screen and (max-width: 600px) {
     .container{
       padding:5rem 1%;
     }
  h2{
    font-size:1.5rem;
  }
  .get-started{
    padding:1rem;
  }
  }
</style>

<section class="get-started">
  <h2>Ready to get Started</h2>
  <p>
  Sign Up on clearIT to easily get access to logistics services and enjoy streamless shipping experiences
  </p>
  <div class="button">
   <a href='/'>GET STARTED</a>
  </div>
</section>
<footer>
  <div class="container">
    <FooterContent />
  </div>
</footer>
