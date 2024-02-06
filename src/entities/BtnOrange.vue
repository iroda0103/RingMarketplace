<template>
  <button class="btn_orange"> {{text}} </button>
</template>

<script>
export default {
  props: {
    text: String,
  },
};
</script>

<style>

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

.btn_orange:hover{
    cursor:pointer;
    transform: scale(1.02);
}
</style>
