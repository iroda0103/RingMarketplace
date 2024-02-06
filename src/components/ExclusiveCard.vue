<template>
  <div class="exclusive_card">
    <img :src="item.img" class="exclusive_card--img" />
    <div class="exclusive_card__body">
      <h4>{{ item.name }}</h4>
      <p class="exclusive_card--paragraph">{{ item.price }}</p>
      <div class="exclusive_card__wrapper">
        <img src="../assets/images/exclusive_avatar.svg" />
        <p class="exclusive_author_name">Darrell Steward</p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    item: Object,
  },
};
</script>
<style>
.exclusive_card {
  max-width: 310px;
  width: 100%;
  background: #f4f4f4;
  box-shadow: 12px 18px 30px rgba(0, 0, 0, 0.1);
  border-radius: 20px;
}
.exclusive_card:hover {
  box-shadow: 0 24px 38px 3px rgba(0, 0, 0, 0.14),
    0 9px 46px 8px rgba(0, 0, 0, 0.12), 0 11px 15px -7px rgba(0, 0, 0, 0.2);
  /* filter: brightness(110%); */
}

.exclusive_card__wrapper {
  display: flex;
  /* justify-content: space-between; */
  align-items: center;
  gap: 15px;
}

.exclusive_card__body {
  padding: 30px;
}

.exclusive_card h4 {
  font-weight: 700;
  font-size: 18px;
  text-align: left;
  color: #232222;
}

.exclusive_card--paragraph {
  font-weight: 700;
  font-size: 24px;
  color: #ff8e1e;
  text-align: left;
  margin: 10px 0 20px 0;
}

.exclusive_card--img {
  border-radius: 20px;
}

.exclusive_author_name {
  font-weight: 700;
  font-size: 16px;
  line-height: 175.4%;
  color: #232222;
}
</style>
