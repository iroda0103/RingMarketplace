<template>
  <section class="blog">
    <div class="blog__header">
      <div>
        <h2 class="header_text">Now With More News and Blogs</h2>
        <p class="paragraph">
          This NFT website is a website that features buying and selling, news
          and blogs. Designed with a minimalist and informative concept
        </p>
      </div>
      <div>
        <button class="blog_btn" @click="changedClass">{{ btn_text }}</button>
      </div>
    </div>
    <div :class="class_group">
      <BlogCard v-for="item in data" :item="item" :key="item.id"></BlogCard>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";
import BlogCard from "./BlogCard.vue";

const data = ref([
  {
    id: 1,
    name: "Theresa Webb",
    img: "src/assets/images/blog_img_1.png",
    isActive: false,
  },
  {
    id: 2,
    name: "Eleanor Pena",
    img: "src/assets/images/blog_img_2.png",
    isActive: true,
  },
  {
    id: 3,
    name: "Darlene RobertsonThere",
    img: "src/assets/images/blog_img_1.png",
    isActive: false,
  },
  {
    id: 4,
    name: "Theresa Webb",
    img: "src/assets/images/blog_img_1.png",
    isActive: false,
  },
  {
    id: 5,
    name: "Theresa Webb",
    img: "src/assets/images/blog_img_1.png",
    isActive: false,
  },
  {
    id: 6,
    name: "Eleanor Pena",
    img: "src/assets/images/blog_img_2.png",
    isActive: true,
  },
]);

const class_group = ref("blog_card_group");
const btn_text = ref("See All");
const is_btn_click = ref(false);

function changedClass() {
  if (!is_btn_click.value) {
    class_group.value = "blog_card_group blog_card_group_all";
    btn_text.value = "See Narrow";
  } else {
    class_group.value = "blog_card_group";
    btn_text.value = "See All";
  }
  is_btn_click.value = !is_btn_click.value;
}
</script>

<style>
@keyframes identifier {
  0% {
  }
  100% {
    transform: translateX(calc(-100%+392px));
  }
}

.blog_btn {
  background: linear-gradient(0deg, rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.2)),
    linear-gradient(140.08deg, #9cd2ee 3.42%, #00acee 95.98%);
  border-radius: 10px;
  font-weight: 700;
  font-size: 20px;
  color: #ffffff;
  padding: 15px 30px;
  border: none;
}

.blog .header_text {
  padding-top: 0;
  max-width: 850px;
  text-align: left;
}

.blog__header {
  display: flex;
  align-items: flex-start;
  justify-content: space-around;
  padding-top: 60px;
}

.blog .paragraph {
  text-align: left;
  margin: 0;
}

.blog_card_group {
  display: flex; /* Flex bo'lmagan */
  gap: 30px;
  transform: translateX(-392px);
  margin-top: 50px;
  animation: identifier 22s infinite;
  animation-delay: 0;
  transition: 13s;
  animation-timing-function: linear;
}

.blog {
  max-width: 1440px;
  width: 100%;
  overflow: hidden;
  margin: 0 auto;
}

.blog_card_group_all {
  flex-wrap: wrap;
  transform: translateX(0);
  justify-content: center;
  gap: 50px;
  width: 100%;
  animation: none;
  transition: none;
}
</style>
