<template>
    <div>
         <intro-header-app :boldHead="spanEl" :heading="heading" :subInfo="subInfo"></intro-header-app>
         <div class="product-view-container">
             <div class="product-view">
                 <div class="product-image">
                     <!-- image here -->
                    <img :src="require('@/assets/img/products/' + product.image)" alt="" class="img-responsive">
                 </div>
                 <div class="product-details">
                     <h4>{{ product.name }}</h4>
                     <div class="product-reviews">
                        <div>
                            <p>***** <span class="reviews-received"></span> Review(s)</p>
                        </div>
                        <span>|</span>
                        <div>
                            <a href="#">Add a Review</a>
                        </div>
                        <span>|</span>
                         <div><span>Share:</span>
                            <a href="#"><i class="fab fa-facebook-f"></i></a>
                            <a href="#"><i class="fab fa-twitter"></i></a>
                            <a href="#"><i class="fab fa-google-plus-g"></i></a>
                            <a href="#"><i class="fab fa-pinterest"></i></a>
                            <a href="#"><i class="fab fa-instagram"></i></a>
                            <a href="#"><i class="fas fa-envelope"></i></a>
                        </div>    
                     </div>
                     <span class="product-price">{{ product.price }}</span>
                     <div class="product-stockinfo">
                        <p>Availability: <span>{{product.availability}}</span></p>
                        <p>Product code: <span>{{product.id}}</span></p>
                        <p>Tags: <span>{{product.tags}}</span></p>
                     </div>
                     <div class="product-description">
                        <p>{{product.shortDescription}}
                        </p>
                        <ul>
                            <li>- {{ product.descriptionPerks[0] }}</li>
                            <li>- {{ product.descriptionPerks[1] }}</li>
                            <li>- {{ product.descriptionPerks[2] }}</li>
                            <li>- {{ product.descriptionPerks[3] }}</li>
                        </ul>
                     </div>
                     <div class="product-specification">
                         <div class="product-select">
                             <label for="color">Color</label>
                             <select name="" id="">
                                 <option value="red">{{ product.color[0] }}</option>
                                 <option value="red">{{ product.color[1] }}</option>
                                 <option value="red">{{ product.color[2] }}</option>
                             </select>
                         </div>
                         <div class="product-select">
                             <label for="size">Size</label>
                             <select name="" id="">
                                 <option value="s">{{ product.sizes[0] }}</option>
                                 <option value="m">{{ product.sizes[1] }}</option>
                                 <option value="l">{{ product.sizes[2] }}</option>
                             </select>
                         </div>
                         <div class="product-input">
                             <label for="quantity">Qty</label>
                             <input type="number" name="" id="">
                         </div>
                     </div>
                     <div class="product-view__buttons">
                         <button class="add--tocart"><i class="fas fa-shopping-cart"></i> Add to cart</button>
                         <button class="add--tolookbook"><i class="far fa-heart"></i> Add to lookbook</button>
                     </div>
                     <div class="product-view__compare">
                         <a href="#"><i class="fas fa-compress-arrows-alt"></i> Add to compare</a>
                     </div>
                 </div>
             </div>
             <div class="product-tabs-container">
                 <div id="tabs">
                     <a v-on:click="activeTab=1" v-bind:class="[activeTab === 1 ? 'active' : '']">Description</a>
                     <a v-on:click="activeTab=2" v-bind:class="[activeTab === 2 ? 'active' : '']">Video</a>
                     <a v-on:click="activeTab=3" v-bind:class="[activeTab === 3 ? 'active' : '']">Size &amp; Specs</a>
                     <a v-on:click="activeTab=4" v-bind:class="[activeTab === 4 ? 'active' : '']">Delivery &amp; Returns</a>
                     <a v-on:click="activeTab=5" v-bind:class="[activeTab === 5 ? 'active' : '']">Reviews</a>
                 </div>
                 <div id="tab-content">
                     <div v-if="activeTab === 1" class="description-tab tab d-none">
                         <span class="attention-text">{{ product.longDescription.highlightText }}</span>
                         <p>{{ product.longDescription.longText }}</p>
                     </div>
                     <div v-if="activeTab === 2" class="video-tab tab  d-none">
                         <a :href="(product.video)" target="_blank">Promo video</a>
                     </div>
                     <div v-if="activeTab === 3" class="size-tab tab  d-none">
                         <p>{{ product.sizeTab }}</p>
                     </div>
                     <div v-if="activeTab === 4" class="delivery-tab tab  d-none">
                         <span class="attention-text">Free Shipping Information</span>
                        <p>{{ product.delivery}} </p>
                     </div>
                     <div v-if="activeTab === 5" class="review-tab tab  d-none">
                         <span class="attention-text">Glorious reviews</span>
                         <p>{{ product.reviews }}</p>
                     </div>
                 </div>
             </div>
         </div>
    </div>
</template>

<script>
import HeaderIntro from '../components/HeaderIntro.vue'
import axios from "axios";
export default {
     data() {
        return {
            spanEl: "Product",
            heading: "view",
            subInfo: "Gender - Category - Subcategory - Product",
            activeTab: 1,
            product: {}
        };
    },
    created() {
        this.getData();
  },

  methods: {
    getData() {
        let productId = this.$route.params.id; //grab parameter id from the URL
        axios
        .get("https://my-json-server.typicode.com/HamDerAndrew/vue-ecommerce-prototype/products/" + productId)
        .then(response => {
            this.product = response.data;
        }) 
        .catch(err => console.log(err.message));
    }
  },

    components: {
        "intro-header-app": HeaderIntro
    }
}
</script>

<style lang="scss">

</style>
