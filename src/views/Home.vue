<template>
  <div class="home">
    <div class="promo-slider">
      <img src="../assets/img/avecover-min.jpg" class="img-responsive">
      <button class="slide-btn">Shop Men's collection</button>
    </div>
    <section id="product-section">
      <div class="product-displays">
        <hr>
        <ul class="product-display__list">
          <li><a href="#">popular</a></li>
          <li><a href="#">new arrivals</a></li>
          <li><a href="#">best sellers</a></li>
          <li><a href="#">special offers</a></li>
          <li><a href="#">coming soon</a></li>
        </ul>
        <div id="popular">
          <div v-for="product in products" :key="product.id">
            <!-- image -->
            <router-link :to="'/productview/' + product.id"><img :src="require('@/assets/img/products/' + product.image)" alt="" class="img-responsive"></router-link>
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
           <!-- image hardcoded due to data limit in db reached -->
           <router-link to="/productview/"><img src="../assets/img/products/item 4.png" alt="" class="img-responsive"></router-link>
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
            <!-- image hardcoded due to data limit in db reached -->
           <router-link to="/productview/"><img src="../assets/img/products/item 1.png" alt="" class="img-responsive"></router-link>
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
            <!-- image hardcoded due to data limit in db reached -->
            <router-link to="/productview/"><img src="../assets/img/products/item 6.png" alt="" class="img-responsive"></router-link>
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
            <h2><span>Men's</span> lookbook</h2>
            <p>Lorem ipsum dolor sit amet eras facilisis
              consectetur adipiscing elit lor, integer lorem consecteur dignissim laciniqui.
              Elementum metus facilisis ut phasellu.
            </p>
            <button class="lookbook--btn">View now</button>
          </div>
        </div>
        <div>
          <img src="../assets/img/products/womenslook.png" alt="" class="img-responsive">
          <div class="look-info">
            <h2><span>Women's</span> lookbook</h2>
            <p>Lorem ipsum dolor sit amet eras facilisis
              consectetur adipiscing elit lor, integer lorem consecteur dignissim laciniqui.
              Elementum metus facilisis ut phasellu.
            </p>
            <button class="lookbook--btn">View now</button>
          </div>
        </div>
        <div>
          <img src="../assets/img/products/yourlook.png" alt="" class="img-responsive">
          <div class="look-info">
            <h2><span>Your</span> lookbook</h2>
            <p>Lorem ipsum dolor sit amet eras facilisis
              consectetur adipiscing elit lor, integer lorem consecteur dignissim laciniqui.
              Elementum metus facilisis ut phasellu.
            </p>
            <button class="lookbook--btn">View now</button>
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
@import "@/scss/_mixins.scss";

.product-information {
  visibility: hidden;
}

#product-section {
  width: 65%;
  margin: auto;
}

.product-display__list {
  font-family: $fontHeader;
  padding: 0 10px 0 0;
  text-transform: uppercase;
  font-size: 12px;
  text-align: left;
  font-weight: bold;
  color: $listTextColor;
  letter-spacing: .5px;
  cursor: pointer;
  margin: 30px 0;
  li {
    display: inline-block;
    margin-right: 20px;
    &:hover, &:active {
      color: $linkStates;
    }
    a {
      text-decoration: none;
      color: $listTextColor;
    }
  }
}

#popular {
  display: grid;
  // grid-template-rows: repeat(3, minmax(1fr, 5fr)) ;
  grid-row: auto;
  grid-template-columns: repeat(12, 1fr);
  grid-column-gap: 10px;
  div {
    position: relative;
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
      top: 10%;
      right: 10px;
      text-align: right;
      h2 {
        font-size: 35px;
        span {
          font-weight: bold;
        }
      }
      .lookbook--btn {
        width: 150px;
        height: 50px;
        @include ctaButton;
      }
    }
  }
}

</style>


<script>
// @ is an alias to /src
import axios from "axios";

export default {
  name: 'home',
  data() {
    return {
      products: []
    };
  },

  created() {
    this.getData();
  },

  methods: {
    getData() {
        axios
        .get("https://my-json-server.typicode.com/HamDerAndrew/vue-ecommerce-prototype/products/")
        .then(response => {
            this.products = response.data;
            console.log(response);
        }) 
        .catch(err => console.log(err.message));
    }
  }
}
</script>
