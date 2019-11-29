<style type="text/scss">
  .footer,
  .footer-info {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
  .footer {
    padding: 40px 50px;
  }
  .footer-item {
    display: flex;
    flex-direction: column;
    padding: 0;
    max-width: 33%;
    box-sizing: border-box;
    justify-content: end;
    div {
      margin-bottom: 1rem;
    }
  }
  h3 {
    margin-bottom: 1.5rem;
    font-family: Sailec;
  }
  .logo-cont,
  .footer-info {
    width: 40%;
  }
  .logo-cont{
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }
  .logo {
    font-size: 2.5rem;
  }
  a {
    color: #000;
    opacity: 0.8;
    // opacity:0.5;
    font-size: 11px;
  }
  p{
    font-size: 11px;
  }
  .address{
    position: absolute;
    bottom:10px;
  }
   @media screen and (max-width: 600px) {
   .footer{
     flex-direction: column;
   }
   .footer-info{
     width:100%;
   }
  }
</style>

<div class="footer">
  <div class="logo-cont">
    <div class="logo">ClearIT</div>
    <div class="address">
      <p>1 Adedeji Adekola Street, Lekki, Lagos.</p>
      <p>
        77 King Street West, Suite 400, Toronto-Dominion Centre, Toronto, ON,
        M5K 0A1.
      </p>
    </div>
  </div>
  <div class="footer-info">
    <div class="footer-item">
      <h3>Company</h3>
      <div>
        <a href="/">About Us</a>
      </div>
      <div>
        <a href="/">Careers</a>
      </div>
      <div>
        <a href="/">FAQ</a>
      </div>
      <div>
        <a href="/">Security</a>
      </div>
    </div>
    <div class="footer-item">
      <h3>Legal</h3>
      <div>
        <a href="/">Privacy Policy</a>
      </div>
      <div>
        <a href="/">Terms</a>
      </div>
    </div>
    <div class="footer-item">
      <h3>Social</h3>
      <div>
        <a href="/">Twitter</a>
      </div>
      <div>
        <a href="/">Facebook</a>
      </div>
      <div>
        <a href="/">Instagram</a>
      </div>
      <div>
        <a href="/">LinkedIn</a>
      </div>
    </div>
  </div>
</div>
