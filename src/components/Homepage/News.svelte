<script>
  import { fade } from "svelte/transition";
  let isActive1 = true;
  let isActive2 = false;
  let isActive3 = false;

  let img;
  let p;
  let title;
  function change1() {
    isActive1 = true;
    isActive2 = false;
    isActive3 = false;
  }
  function change2() {
    isActive1 = false;
    isActive2 = true;
    isActive3 = false;
  }
  function change3() {
    isActive1 = false;
    isActive2 = false;
    isActive3 = true;
  }

  $: if (isActive1) {
    title = "Tested";
    img = "images/cargo.jpg";
    p =
      "We searched extensively for a provider that could bring secure,trusted payments into our marketplace. ClearIT has not only beenable to do so, but has also offered us unique services that help usdeliver better experiences and results to our customers.";
  }
  $: if (isActive2) {
    title = "Integrity";
    img = "https://www.costamare.com/images/home_slider/slide-3.jpg";
    p =
      "Duis sed viverra massa. Donec sodales metus at mollis mattis. Quisque viverra dolor nulla, ut sodales lacus feugiat in. Nunc nec bibendum nulla,. Fusce ut volutpat libero. Integer vel lacus id lorem pulvinar aliquet sed at enim. Sed nec mauris placerat, condimentum leo ac, varius nibh";
  }
  $: if (isActive3) {
    title = "Dedication";
    img = "https://www.mercari.com/static/shipping/shipping-hero.png";
    p =
      "Duis sed viverra massa. Donec sodales metus at mollis mattis. Quisque viverra dolor nulla, ut sodales lacus feugiat in. Nunc nec bibendum nulla,. Fusce ut volutpat libero. Integer vel lacus id lorem pulvinar aliquet sed at enim. Sed nec mauris placerat, condimentum leo ac, varius nibh";
  }
</script>

<style>
  section {
    margin-bottom: 15rem;
  }

  h3,
  p {
    text-align: center;
    padding: 1rem 2rem;
  }
  h3 {
    font-size: 3rem;
    width: 70%;
    margin: 0 auto;
    margin-top: 10rem;
  }
  .text {
    margin-bottom: 10rem;
  }
  .bg {
    position: relative;
  }
  .flex-cont {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin: 0 auto;
    /* margin-top: 10rem; */
    width: 80%;
    max-width: 1500px;
  }
  .item {
    width: 45%;
    position: relative;
  }
  .bg-image {
    position: absolute;
    top: 0;
    left: 0;
    height: 110%;
    width: 430px;
    background: url(images/staff.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: 20% 60%;
    box-shadow: inset 0 0 0 2000vw rgba(16, 38, 73, 0.7);
    z-index: -1;
  }
  h1 {
    font-size: 2rem;
    margin-top: 15px;
    text-align: center;
  }
  .card {
    position: relative;
    display: flex;
    flex-direction: column;
    /* min-width: 0; */
    word-wrap: break-word;
    background-color: #fff;
    background-clip: border-box;
    border: none;
    border-radius: 10px;
    min-height: 550px;
    margin-top: 5rem;
    z-index: 1;
    width: 450px;
    /* margin-left:5rem; */
  }
  .chosen {
    height: 15rem;
    /* object-fit: cover; */
    margin-bottom: 2rem;
    transition: all 3s;
    border-bottom: 1px solid black;
  }
  .shadow {
    width: 100%;
    height: 100%;
    background: #000000;
    opacity: 0.1;
    -webkit-filter: blur(2.5rem);
    filter: blur(2.5rem);
    position: absolute;
    top: 0;
    right: -2rem;
    bottom: -1.8rem;
  }
  h2 {
    font-size: 2.3rem;
    margin-bottom: 3rem;
  }
  .img-flex {
    display: flex;
    align-items: center;
    justify-content: space-between;
    /* height:40rem; */
  }
  .img-card {
    width: 29%;
    border-radius: 20px;
    overflow: hidden;
    height: 8rem;
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.15);
  }
  .card-content-img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  @media screen and (max-width: 600px) {
    section {
      overflow: hidden;
      padding-bottom: 3rem;
    }
    h3 {
      font-size: 2rem;
      padding: 0;
      width: 90%;
    }
    .flex-cont {
      flex-direction: column-reverse;
      padding-top: 4rem;
    }
    .item {
      width: 100%;
    }
    h2 {
      color: white;
    }
    .card {
      width: unset;
    }
  }
  @media screen and (min-width: 600px) and (max-width: 1200px) {
    h3 {
      width: 90%;
    }
    .card {
      width: unset;
    }
    .bg-image {
      width: 300px;
    }
  }
</style>

<section>
  <h3>Get the perfect shipping logistics services for your shipment</h3>
  <p class="text">
    Optimize your shipment voucher or build your own.Its a win-win
  </p>
  <div class="bg">
    <div class="bg-image" />
    <div class="flex-cont">
      <div class="item">
        <div class="card">
          <h1>{title}</h1>
          <img
            src={img}
            alt="img"
            class="chosen"
            transition:fade={{ delay: 0, duration: 300 }} />
          <p>{p}</p>
        </div>
        <div class="shadow" />
      </div>
      <div class="item card-info">
        <h2>Trusted By over 1000+ businesses and merchants.</h2>
        <div class="img-flex">
          <div class="img-card">
            <img
              src="images/cargo.jpg"
              alt="image"
              class="card-content-img"
              on:click={change1} />
          </div>
          <div class="img-card">
            <img
              src="https://www.costamare.com/images/home_slider/slide-3.jpg"
              alt="image"
              class="card-content-img"
              on:click={change2} />
          </div>
          <div class="img-card">
            <img
              src="https://www.mercari.com/static/shipping/shipping-hero.png"
              alt="image"
              class="card-content-img"
              on:click={change3} />
          </div>
        </div>

      </div>
    </div>
  </div>
</section>
