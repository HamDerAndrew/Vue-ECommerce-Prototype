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
            <a class="disabled-product" href="#"><img src="../assets/img/products/item 4.png" alt="" class="img-responsive"></a>
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
            <a class="disabled-product" href="#"><img src="../assets/img/products/item 1.png" alt="" class="img-responsive"></a>
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
            <a class="disabled-product" href="#"><img src="../assets/img/products/item 6.png" alt="" class="img-responsive"></a>
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
  </div>
</template>

<style lang="scss">

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
