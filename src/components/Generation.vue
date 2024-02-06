<template>
  <section class="container generation">
    <h2 class="header_text">New Generation of Online Shopping</h2>
    <p class="paragraph">
      This NFT website is a website that features buying and selling, news and
      blogs. Designed with a minimalist and informative concept
    </p>
    <div class="generation_card_group">
      <!-- <GenerationCard v-for="item in data" :item="item" :key="item.id" /> -->
      <card
        v-for="item in data"
        :key="item.id"
        :item="item"
        @generate-active="generateActive"
      >
      </card>
    </div>
  </section>
</template>

<script setup>
import GenerationCard from "./GenerationCard.vue";
import card from "./Card.vue";
const isActive = true;
const arr = [1, 2, 3, 4];
const data = [
  { id: 1, img: "src/assets/images/generate_card_green.png", isActive: false },
  { id: 2, img: "src/assets/images/generate_card_red.png", isActive: true },
  { id: 3, img: "src/assets/images/generate_card_pink.png", isActive: false },
  {
    id: 4,
    img: "src/assets/images/generation_card_img_1.png",
    isActive: false,
  },
];

const generateActive = (item) => {
  data[item.id - 1].isActive = !data[item.id - 1].isActive;
  console.log("ss");
};
</script>

<style>
.generation {
  background: #f7f7f7;
  margin: 0 auto;
}
.generation {
  padding: 30px 0;
}
.generation_card_group {
  display: flex;
  gap: 10px;
  text-align: center;
  justify-content: center;
}
.header_text {
  max-width: 488px;
  width: 100%;
  font-weight: 700;
  font-size: 48px;
  line-height: 68px;
  text-align: center;
  letter-spacing: 0.02em;
  color: #232222;
  margin: 0 auto;
  margin-bottom: 40px;
  padding-top: 60px;
}

.paragraph {
  max-width: 770px;
  width: 100%;
  margin: 0 auto;
  text-align: center;
  margin-bottom: 50px;
  font-size: 20px;
  line-height: 163.9%;
  letter-spacing: 0.02em;
}
</style>
