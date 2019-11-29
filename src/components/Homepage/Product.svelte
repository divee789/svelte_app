<script>

</script>

<style type="text/scss">
  section {
    position: relative;
    margin: 7rem auto;
    padding: 10px 0;
    width: 80%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    @media screen and (max-width: 600px) {
      flex-direction: column;
    }
    // opacity: 0.7;
    h3 {
      font-family: firma-bold;
      font-size: 1.6rem;
    }
    .card {
      position: relative;
      width: 32%;
      border-radius: 5px;
      color: #fff;
      overflow: hidden;
      @media screen and (max-width: 600px) {
        width: 100%;
        margin-bottom: 20px;
      }
      h3,
      p {
        padding: 0 2rem;
      }
      img {
        height: 30rem;
        width: 100%;
        // padding-bottom: 3rem;
        object-fit: contain;
        box-sizing: border-box;
       
        @media screen and (max-width: 1200px) {
          height: 20rem;
        }
      }
    }

    .a {
      background: #9ac3ed;
    }
    .b {
      background: #3d94dd;
    }
    .c {
      background: #eaa844;
    }
  }
</style>

<section>
  <div class="card a">
    <h3>Import / Export</h3>
    <p>with ClearIT,no hassles</p>
    <img
      src="https://d2kh7o38xye1vj.cloudfront.net/wp-content/uploads/2019/05/postpaid-banner.png"
      style="margin-left:-7rem" />
    <p>More about our platform solutions</p>
  </div>
  <div class="card b">
    <h3>Import / Export</h3>
    <p>with ClearIT,no hassles</p>
    <img
      src="https://www.movingtransparent.com/wp-content/uploads/2018/07/about.png" />
    <p>More about our platform solutions</p>
  </div>
  <div class="card c">
    <h3>Import / Export</h3>
    <p>with ClearIT,no hassles</p>
    <img
      src="https://1ivu6q1gqh2kndjc23ryof11v5-wpengine.netdna-ssl.com/wp-content/uploads/2018/08/UPS_truck_padded_medium.png"
      alt="lolo" />
    <p>More about our platform solutions</p>
  </div>

</section>
