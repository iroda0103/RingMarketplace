<template>
  <section class="container exclusive">
    <h2 class="header_text">Exclusive NFT.Ring drops</h2>
    <p class="paragraph">
      This NFT website is a website that features buying and selling, news and
      blogs. Designed with a minimalist and informative concept
    </p>

    <div class="generation_card_group">
      <ExclusiveCard
        v-for="item in data"
        :item="item"
        :key="item.id"
      ></ExclusiveCard>
    </div>
  </section>
</template>

<script setup>
import GenerationCard from "./GenerationCard.vue";
import ExclusiveCard from "./ExclusiveCard.vue";

const isActive = true;
const arr = [1, 2, 3, 4];
const data = [
  {
    id: 1,
    name: "Theresa Webb",
    price: "$475.22",
    author: "Darrell Steward",
    avatar: "../assests/images/exclusive_avatar.svg",
    img: "src/assets/images/exclusive_img_1.png",
    isActive: false,
  },
  {
    id: 2,
    name: "Eleanor Pena",
    price: "$710.68",
    author: "Cody Fisher",
    avatar: "src/assests/images/exclusive_avatar.svg",
    img: "src/assets/images/exclusive_img_2.png",
    isActive: true,
  },
  {
    id: 3,
    name: "Darlene RobertsonThere",
    price: "$928.41",
    author: "Esther Howard",
    avatar: "src/assests/images/exclusive_avatar.svg",
    img: "src/assets/images/exclusive_img_3.png",
    isActive: false,
  },
  {
    id: 4,
    name: "Theresa Webb",
    price: "$475.22",
    author: "Darrell Steward",
    avatar: "src/assests/images/exclusive_avatar.svg",
    img: "src/assets/images/exclusive_img_4.png",
    isActive: false,
  },
  {
    id: 5,
    name: "Theresa Webb",
    price: "$475.22",
    author: "Darrell Steward",
    avatar: "../assests/images/exclusive_avatar.svg",
    img: "src/assets/images/exclusive_img_5.png",
    isActive: false,
  },
  {
    id: 6,
    name: "Theresa Webb",
    price: "$475.22",
    author: "Darrell Steward",
    avatar: "src/assests/images/exclusive_avatar.svg",
    img: "src/assets/images/exclusive_img_6.png",
    isActive: true,
  },
  {
    id: 7,
    name: "Theresa Webb",
    price: "$475.22",
    author: "Darrell Steward",
    avatar: "src/assests/images/exclusive_avatar.svg",
    img: "src/assets/images/exclusive_img_7.png",
    isActive: false,
  },
  {
    id: 8,
    name: "Theresa Webb",
    price: "$475.22",
    author: "Darrell Steward",
    avatar: "src/assests/images/exclusive_avatar.svg",
    img: "src/assets/images/exclusive_img_8.png",
    isActive: false,
  },
];
</script>

<style>
.exclusive .header_text {
  max-width: 660px;
}

.exclusive .generation_card_group {
  flex-wrap: wrap;
  gap: 20px;
}
</style>
