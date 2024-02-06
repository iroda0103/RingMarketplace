<template>
  <div class="container stay-loop">
    <div class="text_wrapper">
      <h2 class="stay--header">Stay in the loop</h2>
      <p  class="stay--paragraph">
        Join our mailing list to stay in the loop with our newest feature
        releases, NFT drops, and tips and tricks for navigating NFT.Ring
      </p>
      <label for="loop_search" class="stay_label"
        ><input class="" id="loop_search" /><BtnOrange
          text="Register"
        ></BtnOrange
      ></label>
    </div>
  </div>
</template>

<script setup>
import BtnOrange from "../entities/BtnOrange.vue";
</script>

<style>
.stay-loop {
  background-image: url("src/assets/images/stay_loop.png");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  padding-top: 250px;
  padding-left: 50px;
  padding-bottom: 120px;
}

.stay-loop .text_wrapper {
  max-width: 495px;
  width: 100%;
}

.stay--header {
  max-width: 420px;
  width: 100%;
  font-weight: 700;
  font-size: 48px;
  line-height: 68px;
  letter-spacing: 0.02em;
  color: #232222;
  margin-bottom: 20px;
}

.stay--paragraph{
    margin-bottom: 50px;
    max-width: 467px;
    width: 100%;
}

#loop_search{
width: 495px;
background: #FFFFFF;
border-radius: 10px;
appearance: none;
border: none;
padding: 15px;
}
#loop_search:focus{
    appearance: none;
    border: none;
    outline: none;
}

.stay-loop .btn_orange{
    position: relative;
    right: 30px;
}

.stay_label{
    position: relative;
    display: flex;
    justify-content: center;
}
</style>
