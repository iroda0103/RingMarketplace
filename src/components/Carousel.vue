<template>
  <div class="carousel">
    <div class="inner">
      <div class="card" v-for="card in cards" :key="card">
        {{ card }}
      </div>
    </div>
  </div>
  <button>prev</button>
  <button @click="next">next</button>
</template>

<script>
export default {
  data() {
    return {
      cards: [1, 2, 3, 4, 5, 6, 7, 8],
      innerStyles: {},
      step: "",
      transitioning: false,
    };
  },
  mounted() {
    this.setStep();
    this.resetTranslate();
  },

  methods: {
    setStep() {
      const innerWidth = this.$refs.inner.scrollWidth; // ❶
      const totalCards = this.cards.length;
      this.step = `${innerWidth / totalCards}px`; // ❷
    },

    next() {
      if (this.transitioning) return;

      this.transitioning = true;
      this.moveLeft(); // ❸
      this.afterTransition(() => {
        // ❶
        const card = this.cards.shift(); // ❷
        this.cards.push(card); // ❸
        this.resetTranslate();
        this.transitioning = false;
      });
    },
    afterTransition(callback) {
      const listener = () => {
        // ❹
        callback();
        this.$refs.inner.removeEventListener("transitionend", listener);
      };
      this.$refs.inner.addEventListener("transitionend", listener); // ❺
    },
 resetTranslate () {
  this.innerStyles = {
    transition: 'none',
    transform: `translateX(-${this.step})`
  }
},
    moveLeft() {
      this.innerStyles = {
        transform: `translateX(-${this.step})
                translateX(-${this.step})`, // ❶
      };
    },

    moveRight() {
      this.innerStyles = {
        transform: `translateX(${this.step})
                translateX(-${this.step})`, // ❷
      };
    },
  },
};
</script>
<style>
.carousel {
  width: 170px; /* ❶ */
  overflow: hidden; /* ❷ */
}

.inner {
  white-space: nowrap; /* ❸ */
  transition: transform 0.2s;
}

.card {
  width: 40px;
  margin-right: 10px;
  display: inline-flex;

  /* optional */
  height: 40px;
  background-color: #39b1bd;
  color: white;
  border-radius: 4px;
  align-items: center;
  justify-content: center;
}

/* optional */
button {
  margin-right: 5px;
  margin-top: 10px;
}
</style>
