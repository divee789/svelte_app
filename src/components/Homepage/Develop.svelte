<style>
  section {
    background: #eaf4ff;
  }
  .container {
    margin: 0 auto;
    padding: 92px 15px;
    width: 100%;
  }
  h3 {
    font-size: 32px;
    font-weight: 700;
    text-align: center;
    margin: 0 auto;
    margin-bottom: 1rem;
    color: #151027;
    max-width: 650px;
  }
  .caption {
    font-size: 16px;
    line-height: 1.6;
    text-align: center;
    max-width: 466px;
    color: #fff;
    margin: 0 auto;
    margin-bottom: 72px;
  }
  .list {
    display: flex;
    justify-content: space-around;
   margin:2rem auto 0;
   width:100%;
   padding:1rem;
  }
 
  .list-item {
    display: flex;
    flex-direction: column;
    width:23%;
     text-align:left;
     margin:1.25rem 0;
     margin-bottom:7rem;
  }
  img {
    width: 30%;
    vertical-align: middle;
  }
  .list-content-title {
    font-size: 1.6rem;
  margin:1.25rem 0;
  font-weight:600;
    color: #151027;
  }
  .list-content-caption {
    font-size: 13px;
    color: #151027;
    line-height: 1.5;
    margin: 0;
    opacity:0.7;
  }
  .actions {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .item {
    margin: 0 8px;
  }
  a {
    padding: 14px 20px !important;
    line-height: unset;
    text-align: center;
    width: 12rem;
  }
  .q {
    background: #fff;
  }
  .w {
    background: var(--background);
    color: #fff;
  }
   @media screen and (max-width:600px){
       .list{
         flex-direction: column;
       }
      .list-item{
        width:100%;
      }
      img{
        width:20%;
      }
      .button{
        width: 100%;
      }
      }
</style>

<section>
  <div class="container">
    <h3>
      We've developed technology you can rely on that grows with your business
    </h3>
    <p class="caption" />
    <div class="list">
      <div class="list-item">
        <div class="list-icon">
          <img src="images/placeholder.svg" alt="place" />
        </div>
        <div class="list-content">
          <div class="list-content-title">Global Reach</div>
          <p class="list-content-caption">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Autem odit
            eos nesciunt aliquid tempora optio quibusdam repellendus quos
            cupiditate omnis illo voluptas nihil sapiente, sit error vitae ipsa
            saepe! Nulla.
          </p>
        </div>
      </div>
      <div class="list-item">
        <div class="list-icon">
          <img src="images/database.svg" alt="place" />
        </div>
        <div class="list-content">
          <div class="list-content-title">One-Time Setup</div>
          <p class="list-content-caption">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta
            earum alias consequatur, quidem, placeat facilis ratione modi
            doloremque asperiores in amet enim laborum autem est suscipit
            exercitationem ipsam! Rem, labore.
          </p>
        </div>
      </div>
      <div class="list-item">
        <div class="list-icon">
          <img src="images/chat.svg" alt="place" />
        </div>
        <div class="list-content">
          <div class="list-content-title">Perfect Match</div>
          <p class="list-content-caption">
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Architecto
            error illum voluptates eos nulla dolor ad odio soluta eum,
            recusandae ullam cumque, veniam culpa. Hic deleniti repellendus enim
            ea maiores!
          </p>
        </div>
      </div>
    </div>
    <div class="actions">
      <div class="item">
        <a href="/" class="button q">CREATE ACCOUNT</a>
      </div>
      <div class="item">
        <a href="/" class="button w">CONTACT US</a>
      </div>
    </div>
  </div>
</section>
