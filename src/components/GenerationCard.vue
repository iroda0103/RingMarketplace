<template>
  <div
    :class="['generation__card card-wrap', { active__card: item.isActive }]"
    @click="clicked(item.isActive)"
    @mousemove="handleMouseMove"
    @mouseenter="handleMouseEnter"
    @mouseleave="handleMouseLeave"
    ref="card"
  >
    <img :src="item.img" />
    <p :class="['generation_card_text', { active_card_text: item.isActive }]">
      Green Ring
    </p>
  </div>
</template>

<style>
.generation__card {
  max-width: 310px;
  width: 100%;
  background: #f7f7f7;
  border-radius: 20px;
}

.active__card {
  background: linear-gradient(132.95deg, #ffc301 9.31%, #ff6533 79.4%);
  box-shadow: 12px 18px 30px rgba(0, 0, 0, 0.08);
}

.generation_card_text {
  font-size: 32px;
  font-weight: 700;
  background-color: transparent;
  padding: 20px;
  text-align: center;
}

.active_card_text {
  color: #fff !important;
}
</style>

<script>
export default {
  props: {
    item: Object,
  },
  methods: {
    clicked() {
      this.$emit();
    },
  },
};
</script>
