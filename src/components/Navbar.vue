<template>
  <div class="container header">
    <div class="header_wrapper">
      <div class="logo">
        <span class="logo--circle"></span>
        <p>NFT.Ring</p>
      </div>

      <nav>
        <ul>
          <li><a href="#">Market</a></li>
          <li><a href="#">Activity</a></li>
          <li><a href="#">Feature</a></li>
          <li><a href="#">Community</a></li>
        </ul>
      </nav>
    </div>
    <BtnOrangeVue text='Login'></BtnOrangeVue>
  </div>
</template>
<script setup>
import BtnOrangeVue from "../entities/BtnOrange.vue";
</script>

<style>
.logo--circle {
  width: 40px;
  height: 40px;
  display: inline-block;
  border-radius: 50%;
  background: linear-gradient(0deg, rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.2)),
    linear-gradient(140.08deg, #9cd2ee 3.42%, #00acee 95.98%);
}

.logo p {
  font-weight: 700;
  font-size: 20px;
  line-height: 175.4%;
  letter-spacing: 0.02em;
  color: #ffffff;
}

.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.header nav ul {
  display: flex;
  justify-content: space-between;
  gap: 30px;
}

.header li,
.header a {
  line-height: 175.4%;
  letter-spacing: 0.02em;
  color: #ffffff;
  list-style: none;
  text-decoration: none;
}

nav ul li a,
nav ul li a:after,
nav ul li a:before {
  transition: all 0.5s;
}

.header a {
  position: relative;
}

nav ul li a:after {
  position: absolute;
  bottom: -8px;
  left: 0;
  right: 0;
  margin: auto;
  width: 0%;
  content: ".";
  color: transparent;
  background: #aaa;
  height: 2px;
}
nav ul li a:hover:after {
  width: 100%;
}

.header li:hover {
  /* transform: translateY(-2px);
  transition: 0.4s; */
  cursor: pointer;
}

.logo {
  display: flex;
  gap: 15px;
}

.header_wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 100px;
}
</style>
