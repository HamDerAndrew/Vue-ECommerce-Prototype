<template>
    <div>
        <div id="top-bar">
            <div class="top-bar__container">
                <div class="currency">
                    Currency: 
                    <select name="" id="">
                        <option value="GBP">GBP</option>
                        <option value="Euro">Euro</option>
                        <option value="DKK">DKK</option>
                    </select>
                </div>
                <div class="account-shopping">
                    <div class="account">
                        <router-link to="/registerpage">Sign In</router-link>
                        <router-link to="/registerpage">Register</router-link>
                    </div>
                    <div id="cart">
                        <i class="fas fa-shopping-cart"><span class="cart-items">empty</span></i>
                        <i class="fas fa-caret-down cart-dropdown"></i>
                    </div>
                </div>
            </div>
        </div>
        <div id="main-header"> <!-- Main Header Start -->
            <div class="header-container">
                <div class="logo">
                    <router-link to="/"><span>Avenue</span> Fashion</router-link>
                </div>
                <div class="nav-container">
                    <div class="search-nav-wrap">
                        <nav>
                        <ul id="categories">
                            <li class="category-menu"> <a href="#" class="category--link">Mens <i class="fas fa-caret-down"></i></a>
                                <div class="category-menu__tab"> <!--Mens Products start -->
                                    <div class="category-products">
                                        <div class="category__list">
                                            <h4>Casuals</h4>
                                            <ul v-for="casual in casuals" :key="casual">
                                                <li class="product-item"><a href="#" class="product--link">{{ casual }}</a></li>
                                            </ul>
                                        </div>
                                        <div class="category__list">
                                            <h4>Formals</h4>
                                            <ul v-for="formal in formals" :key="formal">
                                                <li class="product-item"><a href="#">{{ formal }}</a></li>
                                            </ul>
                                        </div>
                                    </div>
                                    <div class="sales-banner">
                                        <p><span>Autumn Sale!</span> up to 50% off</p>
                                    </div>
                                </div> <!-- Mens Products end -->
                            </li>
                            <li class="category-menu"> <a href="#" class="category--link">Womens <i class="fas fa-caret-down"></i></a>
                                <div class="category-menu__tab"> <!-- Womens Products start -->
                                    <div class="category-products">
                                        <div class="category__list">
                                            <h4>Casuals</h4>
                                            <ul v-for="casual in casuals" :key="casual">
                                                <li class="product-item"><a href="#" class="product--link">{{ casual }}</a></li>
                                            </ul>
                                        </div>
                                        <div class="category__list">
                                            <h4>Formals</h4>
                                            <ul v-for="formal in formals" :key="formal">
                                                <li class="product-item"><a href="#">{{ formal }}</a></li>
                                            </ul>
                                        </div>
                                    </div>
                                    <div class="sales-banner">
                                        <p><span>Autumn Sale!</span> up to 50% off</p>
                                    </div>
                                </div> <!-- Womens Products end -->
                            </li>
                            <li class="category-menu"> 
                                    <router-link to="/brand">The Brand</router-link>
                            </li>
                            <li class="category-menu"> <a href="#" class="category--link">Local stores <i class="fas fa-caret-down"></i></a>
                                <div class="category-menu__tab"> <!-- Local Stores start -->
                                    <div class="local-stores"> 
                                        <div class="map" style="text-align: center; margin-bottom:20px;">
                                            <i class="fas fa-map-marked-alt" style="font-size: 50px;"></i>
                                        </div>
                                        <ul v-for="store in localStore" :key="store.id">
                                            <li class="local-stores__location">{{ store.country }} - <a href="#">{{ store.city }}</a></li>
                                        </ul>
                                    </div>
                                </div> <!-- Local Stores end -->
                            </li>
                            <li class="category-menu"> <a href="#" class="category--link">Look book <i class="fas fa-caret-down"></i></a>
                                <div class="category-menu__tab">
                                    <p>LookBook content soon to be published</p>
                                </div>
                            </li>
                        </ul>
                    </nav>
                        <div class="search-field-container">
                            <form action="#">
                                <div class="search-container">
                                    <input type="text" value="search.." class="search--input">
                                    <button id="search-button"><i class="fas fa-search"></i></button>
                                </div>
                            </form>
                        </div>
                    </div>
                </div>
            </div>
        </div> <!-- Main header End -->
    </div>
</template>

<script>
export default {
    data() {
        return {
            casuals: ['Jackets', 'Hoodies & Sweatshirts', 'Polo Shirts', 'Sportswear', 'Trousers & Chinos', 'T-shirts'],
            formals: ['Jackets', 'Shirts', 'Suits', 'Trousers'],
            localStore: [
                {id: 1, country: 'Denmark', city: 'Copenhagen'},
                {id: 2, country: 'Sweden', city: 'Stockholm'},
                {id: 3, country: 'Norway', city: 'Oslo'},
                {id: 4, country: 'England', city: 'London'}
            ]
        };
    }
}
</script>

