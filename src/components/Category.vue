<template>
  <section class="container category">

    <h2 class="header_text">Browse by category</h2>
    <p class="paragraph">
      This NFT website is a website that features buying and selling, news and
      blogs. Designed with a minimalist and informative concept
    </p>

    <div class="generation_card_group">
      <img v-for="item in data" :key="item.id" :src="item.img" />
    </div>

  </section>
</template>

<script setup>
import GenerationCard from "./GenerationCard.vue";

const isActive = true;
const data = [];

for (let i = 1; i < 17; i++) {
  data.push({
    id: i,
    isActive: false,
    img: `src/assets/images/category_galery_${i}.png`,
  });
}
</script>

<style>

.category .header_text {
  max-width: 520px;
  padding-top: 0;
}

.category .generation_card_group {
  flex-wrap: wrap;
}
.category .generation_card_group img{
    border-radius: 20px;
}
.category .generation_card_group img:hover {
  cursor: pointer;
  box-shadow: 0 24px 38px 3px rgba(0, 0, 0, 0.14),
    0 9px 46px 8px rgba(0, 0, 0, 0.12), 0 11px 15px -7px rgba(0, 0, 0, 0.2);
    filter: brightness(110%);
}
</style>
