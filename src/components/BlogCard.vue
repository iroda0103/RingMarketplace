<template>
  <div class="blog-card">
    <img :src="item.img" />
    <div class="blog-card__wrapper"><p>What's in Store for NFT</p></div>
  </div>
</template>
<script>
export default {
  props: {
    item: Object,
  },
};
</script>

<style setup>
.blog-card {
  background-image: url("src/assets/images/blog_img_1.png");
  height: 452px;
  width: 530px;
  /* width: 100%; */
  position: relative;
}

.blog-card__wrapper {
  bottom: 0;
  left: 0;
  position: absolute;
  width: 310px;
  height: 108px;
  background: #f4f4f4;
  padding: 30px 50px;
}
.blog-card__wrapper p {
  font-weight: 700;
  font-size: 24px;
  line-height: 141.9%;
  letter-spacing: 0.02em;
  color: #232222;
}
</style>
