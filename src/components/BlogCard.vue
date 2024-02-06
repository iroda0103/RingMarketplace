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
  height: 452px;
  width: 530px;
  position: relative;
  /* overflow: hidden; */
}

.blog-card:hover {
  cursor: pointer;
  box-shadow: 0 24px 38px 3px rgba(0, 0, 0, 0.14),
    0 9px 46px 8px rgba(0, 0, 0, 0.12), 0 11px 15px -7px rgba(0, 0, 0, 0.2);
  filter: brightness(110%);
}
.blog-card img{
   height: 452px;
  width: 530px;
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
