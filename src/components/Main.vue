<script setup>
import BtnOrangeVue from "@/entities/BtnOrange.vue";
import Navbar from "./Navbar.vue";
import Note from "./Note.vue";
</script>
<template>
  <div class="container main">
    <Navbar></Navbar>
    <div class="main__text">
      <h1>The Home of Minimalist Buying and Selling</h1>
      <p>
        This NFT website is a website that features buying and selling, news and
        blogs. Designed with a minimalist and informative concept
      </p>
      <div class="main_btn__group">
        <button class="btn_orange">Explore</button>
        <button class="btn_transparent" @click="changed()">Create</button>
      </div>
    </div>
    <Note>
  </div>
</template>

<style>
.main {
  background-image: url("../assets/images/main_bg_img.png");
  height: 832px;
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  padding: 40px 120px;
  position: relative;
}

.main__text {
  max-width: 480px;
  width: 100%;
  margin-top: 132px;
  display: flex;
  flex-direction: column;
  gap: 30px;
}

.main__text h1,
.main__text p {
  color: #fff;
}

.main__text h1 {
  font-weight: 700;
  font-size: 48px;
  line-height: 68px;
  letter-spacing: 0.02em;
}

.main_btn__group {
  display: flex;
  align-items: center;

  gap: 20px;
}

.btn_transparent {
  border: 1px solid #ff8e1e;
  border-radius: 10px;
  background: transparent;
  color: #fff;
  padding: 14px 20px;
  font-weight: 700;
  line-height: 175.4%;
  letter-spacing: 0.02em;
}

.btn_transparent:hover{
  cursor:pointer;
  transform: scale(1.03);
  transition: 0.2s;

  background: linear-gradient(132.95deg, #FFC301 9.31%, #FF6533 79.4%);
box-shadow: 15px 15px 35px rgba(226, 142, 15, 0.18);
border-radius: 10px;
padding: 15px 25px;
border:none;
font-weight: 700;
line-height: 175.4%;
letter-spacing: 0.02em;
color: #F4F4F4;
transition: 0.2s;
}

.btn_orange{
background: linear-gradient(132.95deg, #FFC301 9.31%, #FF6533 79.4%);
box-shadow: 15px 15px 35px rgba(226, 142, 15, 0.18);
border-radius: 10px;
padding: 15px 25px;
border:none;
font-weight: 700;
line-height: 175.4%;
letter-spacing: 0.02em;
color: #F4F4F4;
transition: 0.2s;
}
</style>
