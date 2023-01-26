<template>
  <div class="header">
    <div class="col">
      <h3>Has just arrived!</h3>
      <h1>Huge Summer Collection</h1>
      <p>Swimmer, Tops, Short, Sunglasses & much more</p>
      <button class="shop-now">Shop Now <i class="fa-solid fa-angle-right"></i></button>
    </div>
    <div class="col">
        <img src="../assets/01.jpg">
    </div>
  </div>

  <Gallery />

  <div class="content">
    <div class="col-1">
      <div>
        <a href=""><i class="fa-brands fa-facebook"></i></a>
        <h2>Follow us on facebook</h2>
      </div>
    </div>
    <div class="col-2">
      <div>
        <a href=""><i class="fa-brands fa-instagram"></i></a>
        <h2>Follow us on facebook</h2>
      </div>
    </div>
    
    </div>
</template>
<script>
import Gallery from './Gallery.vue'
export default {
    components: {
        Gallery
    }
}
</script>
<style scoped>
body {
    padding: 0;
    margin: 0;
}
.header {
    background: #3AAFD2;
    position: absolute;
    top: 140px;
    width: 100%;
    height: 700px;
    display: flex;
}
.col {
    flex: 50%;
    width: 600px;
    overflow: hidden;
}
.col img {
    position: relative;
}
.col h3 {
    position: absolute;
    top: 150px;
    color: #fff;
    font-size: 35px;
    user-select: none;
    opacity: 0;
    animation-name: header3;
    animation-duration: 1s;
    animation-direction: normal;
    animation-fill-mode: forwards;
}
.col h1 {
    position: absolute;
    top: 200px;
    color: #fff;
    font-size: 50px;
    opacity: 0;
    user-select: none;
    animation-name: header1;
    animation-duration: 1s;
    animation-delay: .3s;
    animation-fill-mode: forwards;
}
.col p {
    position: absolute;
    top: 270px;
    color: #fff;
    font-size: 20px;
    opacity: 0;
    user-select: none;
    animation-name: para;
    animation-duration: 1s;
    animation-delay: .5s;
    animation-fill-mode: forwards;
}
.shop-now {
    position: absolute;
    top: 350px;
    left: 60px;
    border: none;
    outline: none;
    border-radius: 5px;
    color: white;
    font-size: 16px;
    font-weight: 600;
    background-color: #fe696a;
    animation-name: btn;
    animation-duration: .7s;
    animation-delay: 1s;
    opacity: 0;
    cursor: pointer;
    animation-fill-mode: forwards;
}
.shop-now:hover {
    background: red;
}
.shop-now i {
    font-size: 16px;
}
@keyframes btn {
from {
    padding: 7px 11px;
    top: 360;
    left: 60px;
    opacity: 0;
}
to {
    padding: 14px 25px;
    top: 350px;
    left: 50px;
    opacity: 1;
   }
}
@keyframes header1 {
from { left: 10px; opacity: 0; }
to {left: 50px; opacity: 1;}
}
@keyframes header3 {
from { left: 10px; opacity: 0; }
to {left: 50px; opacity: 1;}
}
@keyframes para {
from { left: 10px; opacity: 0;}
to {left: 50px; opacity: 1;}
}
.content {
      position: absolute;
      top: 1900px;
      display: flex;
      flex-wrap: wrap;
      width: 100%;
      height: 200px;
      background: red;
      text-align: center;
      color: #4b566b;
    }
    .col-1 {
      flex-basis: 50%;
      display: flex;
      justify-content: center;
      align-items: center;
      background: rgb(245, 233, 233);
    }
    .col-2 {
      background: rgb(238, 231, 245);
      flex-basis: 50%;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    .content i {
      flex-basis: 100%;
      font-size: 40px;
    }
    .col-1 a {
      color: #0f56da;
      margin: 10px 0;
    }
    .col-2 a {
      color: rgb(204, 66, 186);
    }
.footer {
    position: absolute;
    top: 2100px;
    width: 100%;
    height: 800px;
    background: #091b3d;
    color: #fff;
    display: flex;
}
.footer ul {
    flex-basis: 33%;
    margin: 50px 25px;
}
.footer li {
    margin: 15px 0px;
    font-size: 16px;
    color: #555;
}
</style>