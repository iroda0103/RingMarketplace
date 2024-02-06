<template>
  <div class="container partners">
    <div class="partners_group">
      <img v-for="item in data" :key="item.id" :src="item.img" />
    </div>
  </div>
</template>
<script setup>
const data = [
  { id: 1, img: "src/assets/images/partners_img_1.svg" },
  { id: 2, img: "src/assets/images/partners_img_2.svg" },
  { id: 3, img: "src/assets/images/partners_img_3.svg" },
  { id: 4, img: "src/assets/images/partners_img_4.svg" },
  { id: 5, img: "src/assets/images/partners_img_5.svg" },
  { id: 1, img: "src/assets/images/partners_img_1.svg" },
  { id: 2, img: "src/assets/images/partners_img_2.svg" },
  { id: 3, img: "src/assets/images/partners_img_3.svg" },
  { id: 4, img: "src/assets/images/partners_img_4.svg" },
  { id: 5, img: "src/assets/images/partners_img_5.svg" },
];
</script>

<style>
@keyframes identifier {
  0% {
  }
  100% {
    transform: translateX(-1440px);
  }
}
.partners {
  background: #f4f4f4;
  margin-top: 50px;
  overflow: hidden;
}
.partners_group {
  display: flex;
  gap: 80px;
  justify-content: space-between;
  padding: 50px;
  animation: identifier 22s infinite;
  animation-delay: 0;
  transition: 13s;
  animation-timing-function: linear;
}
</style>
