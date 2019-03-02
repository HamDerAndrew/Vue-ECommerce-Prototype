<template>
  <div class="home">
    <div class="promo-slider">
      <img src="../assets/img/avecover-min.jpg" class="img-responsive">
      <button class="slide-btn">Shop Men's collection</button>
    </div>
    <section id="product-section">
      <div class="product-displays">
        <ul class="product-display__list">
          <li><a>popular</a></li>
          <li><a>new arrivals</a></li>
          <li><a>best sellers</a></li>
          <li><a>special offers</a></li>
          <li><a>coming soon</a></li>
        </ul>
        <div id="popular">
          <div>
            <!-- image -->
            <img src="../assets/img/products/item 1.png" alt="">
            <div class="product-information">
              <!-- product content on :hover here -->
              <div class="product-information__icons">
                <div class="circle">
                  <i class="fas fa-shopping-cart"></i>
                </div>
              </div>
            </div>
          </div>
          <div>
            <!-- image -->
            <img src="../assets/img/products/item 2.png" alt="">
            <div class="product-information">
              <!-- product content on :hover here -->
              <div class="product-information__icons">
                <div class="circle">
                  <i class="fas fa-shopping-cart"></i>
                </div>
              </div>
            </div>
          </div>
          <div>
            <!-- image -->
            <img src="../assets/img/products/item 3.png" alt="">
            <div class="product-information">
              <!-- product content on :hover here -->
              <div class="product-information__icons">
                <div class="circle">
                  <i class="fas fa-shopping-cart"></i>
                </div>
              </div>
            </div>
          </div>
          <div>
            <!-- image -->
            <img src="../assets/img/products/item 4.png" alt="">
            <div class="product-information">
              <!-- product content on :hover here -->
              <div class="product-information__icons">
                <div class="circle">
                  <i class="fas fa-shopping-cart"></i>
                </div>
              </div>
            </div>
          </div>
          <div>
            <!-- image -->
            <img src="../assets/img/products/test.png" alt="">
            <div class="product-information">
              <!-- product content on :hover here -->
              <div class="product-information__icons">
                <div class="circle">
                  <i class="fas fa-shopping-cart"></i>
                </div>
              </div>
            </div>
          </div>
          <div>
            <!-- image -->
            <img src="../assets/img/products/item 6.png" alt="">
            <div class="product-information">
              <!-- product content on :hover here -->
              <div class="product-information__icons">
                <div class="circle">
                  <i class="fas fa-shopping-cart"></i>
                </div>
              </div>
            </div>
          </div>
        </div>

      </div>
    </section>
    <section id="look-section">
      <div class="look-section-container">
        <div>
          <img src="../assets/img/products/menslook.png" alt="" class="img-responsive">
          <div class="look-info">
            <h2>Men's lookbook</h2>
            <p>Lorem ipsum dolor sit amet eras facilisis
              consectetur adipiscing elit lor, integer lorem consecteur dignissim laciniqui.
              Elementum metus facilisis ut phasellu.
            </p>
            <button>View now</button>
          </div>
        </div>
        <div>
          <img src="../assets/img/products/womenslook.png" alt="" class="img-responsive">
          <div class="look-info">
            <h2>Women's lookbook</h2>
            <p>Lorem ipsum dolor sit amet eras facilisis
              consectetur adipiscing elit lor, integer lorem consecteur dignissim laciniqui.
              Elementum metus facilisis ut phasellu.
            </p>
            <button>View now</button>
          </div>
        </div>
        <div>
          <img src="../assets/img/products/yourlook.png" alt="" class="img-responsive">
          <div class="look-info">
            <h2>Your lookbook</h2>
            <p>Lorem ipsum dolor sit amet eras facilisis
              consectetur adipiscing elit lor, integer lorem consecteur dignissim laciniqui.
              Elementum metus facilisis ut phasellu.
            </p>
            <button>View now</button>
          </div>
        </div>
      </div>
    </section>
    <!-- <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<style lang="scss">
@import "@/scss/_var.scss";

.product-information {
  visibility: hidden;
}

#product-section {
  width: 65%;
  margin: auto;
}

.product-display__list {
  display: flex;
  width: 50%;
  justify-content: space-between;
}

#popular {
  display: grid;
  // grid-template-rows: repeat(3, minmax(1fr, 5fr)) ;
  grid-row: auto;
  grid-template-columns: repeat(12, 1fr);
  grid-column-gap: 10px;
  div {
    position: relative;
    img {
      max-width: 100%;
      height: auto;
    }
  }
  div:nth-child(1n){
    grid-column: 1 / 4;
    grid-row: 1 / 2;
  }
  div:nth-child(2n){
    grid-column: 4 / 7;
    grid-row: 1 / 2;
  }
  div:nth-child(3n){
    grid-column: 7 / 13;
    grid-row: 1 / 3;
  }
  div:nth-child(4n){
    grid-column: 1 / 7;
    grid-row: 2 / 4;
  }
  div:nth-child(5n){
    grid-column: 7 / 10;
    grid-row: 3 / 4;
  }
  div:nth-child(6n){
    grid-column: 10 / 13;
    grid-row: 3 / 4;
  }
}

//Look Grid
.look-section-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 10px;
  div:nth-child(1n){
    grid-column: 1 / 2;
    position: relative;
  }
  div:nth-child(2n){
    grid-column: 2 / 3;
    position: relative;
  }
  div:nth-child(3n){
    grid-column: 3 / -1;
    position: relative;
  }
  div {
    .look-info {
      position: absolute;
      width: 50%;
      top: 0;
      right: 10px;
    }
  }
}

</style>


<script>
// @ is an alias to /src
//import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home'
  // components: {
  //   HelloWorld
  // }
}
</script>
