<template>
    <router-view />

  <div class="wrapper">
    <nav>   
      <div class="navbar">
        
        <div class="logo">
          <router-link to="/">Cartzilla</router-link>
        </div>

        <div class="search-box">
          <input placeholder="Search for products" type="search" name="" id="">
          <form action="">
            <button class="search-icon">
              <i class="fas fa-search"></i>
            </button>
          </form>
        </div>

        <ul class="nav-links">
          <li class="nav-link"><router-link to="/"><i class="fa-solid fa-heart"></i></router-link></li>
          <li class="nav-link">
              <a class="account" @click="toggleLogin">
                <i class="fas fa-user"></i>
                <div>
                  <p>Hello, {{user.name}}</p>
                  Account
                </div>
              </a>
          </li>
          <li class="nav-link"><router-link :to="{ name: 'Cart' }"><i class="fas fa-shopping-cart"></i>Cart</router-link></li>
       </ul>
      </div>
      
      <div class="categories">
        <ul class="categories-links">
          <li class="categories-link"><a href="">Best Sellers</a></li>
          <li class="categories-link"><a href="">Food</a></li>
          <li class="categories-link"><a href="">Music</a></li>
          <li class="categories-link"><a href="">Books</a></li>
          <li class="categories-link"><a href="">Computers</a>
            <ul>
              <li><a href="">Laptop & Tablets</a></li>
              <li><a href="">Desktop Computers</a></li>
              <li><a href="">Computer External Components</a></li>
                            <li><a href="">Computer Internal Components</a></li>
              <li><a href="">Network Products</a></li>
              <li><a href="">Single boared Computers</a></li>
              <li><a href="">Desktop barebones</a></li>
            </ul>
          </li>
          <li class="categories-link"><a href="">Mobiles & Tablets</a></li>
          <li class="categories-link"><a href="">Video Games</a></li>
          <li class="categories-link"><a href="">TVs</a>
            <ul>
              <li><a href="">TV Sets</a></li>
              <li><a href="">Home Theater Systems</a></li>
              <li><a href="">DVD Players & Recorders</a></li>
              <li><a href="">Blue-ray Players & Recorders</a></li>
              <li><a href="">HD DVD Players & Recorders</a></li>
              <li><a href="">DVD-VCR Combos</a></li>
              <li><a href="">DTV Converters</a></li>
              <li><a href="">AV Receivers</a></li>
              <li><a href="">AV Amplifiers</a></li>
              <li><a href="">Projectors</a></li>
              <li><a href="">Projection Screens</a></li>
            </ul>
          </li>
          <li class="categories-link"><a href="">More</a></li>
        </ul>
      </div>
      
    </nav>
  </div>

  <div v-if="showAccountBox">
    <Login @close="toggleLogin"/>
  </div>

</template>

<script>
import Login from '@/components/Login.vue';
export default {
  components: { Login },
  data() {
    return {
      showAccountBox: false,
      user: {
        name: 'Sign in'
      }
    }
  },
  methods: {
    toggleLogin() {
      this.showAccountBox = !this.showAccountBox;
      this.$emit('hide', this.showAccountBox)
    }
  }

}
</script>

<style>
* {
  padding: 0;
  margin: 0;
  text-decoration: none;
  list-style: none;
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;
}
.wrapper {
  position: fixed;
  width: 100%;
  flex: 1;
  background: #fff;
}
.wrapper nav {
  position: relative;
  display: flex;
  flex-wrap: wrap;
  width: calc(100% - 50px);
  margin: 0 auto;
  justify-content: space-between;
}
.navbar {
  flex: 100%;
  height: 70px;
  display: flex;
  align-items: center;
}
.logo {
  color: #555;
  font-size: 30px;
  font-weight: 600;
  margin-left: 20px;
}
.logo a {
  color: #4b566b;
}
.wrapper nav .navbar .search-box {
  position: relative;
  background: #fff;
  border-radius: 30px;
  width: 100%;
  margin-left: 20px;
  margin-right: 20px;
}
.search-box input[type="search"] {
  height: 48px;
  width: 100%;
  outline: none;
  border: none;
  border-radius: 5px;
  padding: 0 60px 0 20px;
  font-size: 18px;
  box-shadow: 0px 1px 5px rgb(0, 0, 0, .1);
}
.search-box .search-icon {
  position: absolute;
  top: 15px;
  right: 15px;
  text-align: center;
  font-size: 20px;
  color: #644bff;
  border: none;
  outline: none;
  background: white;
  cursor: pointer;
}
.nav-links {
  float: right;
  display: flex;
  align-items: center;
}
.nav-link {
  list-style: none;
}
.nav-link .account {
  font-family: sans-serif;
  border-radius: 5px;
  font-size: 20px;
  border: none;
  outline: none;
  display: flex;
  text-align: left;
}
.account p {
  font-size: 10px;
}
.account i {
  padding-right: 8px;
  font-size: 20px;
}
.nav-link a {
  color: #4b566b;
  font-size: 20px;
  font-weight: 800;
  padding: 10px 25px;
  border-radius: 5px;
  margin: 0 5px; cursor: pointer;
  align-items: center;
  display: flex;
}
.nav-link a i {
  padding: 5px;
}

.categories {
  height: 70px;
  display: flex;
  align-items: center;
  width: 100%;
  box-shadow: 0 4px 2px -2px rgb(0, 0, 0, .1);
}
.categories-links {
  display: flex;
  margin-right: 50px;
  align-items: center;
  margin: 0 auto;
}
.categories-link a {
  display: block;
  color: #4b566b;
  font-size: 18px;
  font-weight: 400;
  padding: 22px 14px;
}
.categories-link a:hover {
  color: #fe696a;
}
.categories-link ul {
  display: none;
  position: absolute;
  padding: 15px;
  border-radius: 4px 4px 4px 4px;
  box-shadow: 0px 1px 5px 3px rgb(0, 0, 0, .1);
  background: #ffffff;
}
.categories-link ul li {
  width: 100%;
}
.categories-link ul li a{
  padding: 8px 14px;
  font-size: 16px;
}
.categories-link ul li a:hover {
 color: #fe696a;
}
.categories-link:hover ul {
  display: block;
}

</style>