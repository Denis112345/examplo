<template>
  <div class="wrapper">
    <div
      class="slider"
      :style="{ background: sliders[sliderCount].background }"
    >
      <button
        @click.prevent="countSliderDown"
        class="slider__prevButton"
        type="submit"
      >
        <img src="@/img/prevSlideBut.png" alt="" />
      </button>

      <div class="slider__offer">
        <h1 class="offer__h1">{{ sliders[sliderCount].title }}</h1>
        <a class="offer__a" href="#">
          {{ sliders[sliderCount].buttonTitle }}
        </a>
      </div>

      <img :src="require(`@/img/${sliders[sliderCount].img}`)" />

      <button
        @click.prevent="countSliderUp"
        class="slider__nextButton"
        type="submit"
      >
        <img src="@/img/nextSlideBut.png" alt="" />
      </button>

      <div class="slider__breake"></div>

      <div class="slider__count">
        <div
          class="eclipse"
          v-bind:class="{ eclipse1_: sliderCount == 0 }"
        ></div>
        <div
          class="eclipse"
          v-bind:class="{ eclipse2_: sliderCount == 1 }"
        ></div>
        <div
          class="eclipse"
          v-bind:class="{ eclipse3_: sliderCount == 2 }"
        ></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "slider",
  data: () => ({
    sliderCount: 1,
    sliders: [
      {
        id: 1,
        title: "Скидки на овощи 15% !",
        buttonTitle: "Перейти в каталог",
        img: "imgSlider2.jpg",
        background: "blue",
      },
      {
        id: 2,
        title: "Дарим скидку в 10% при первом заказе",
        buttonTitle: "Перейти в каталог",
        img: "slider1.png",
        background:
          "linear-gradient(104.81deg, #FFFEFF 20.22%, #F6F9FF 60.49%)",
      },
      {
        id: 3,
        title: "Скидочная карта в подарок",
        buttonTitle: "Узнать больше",
        img: "imgSlider2.jpg",
        background: "yellow",
      },
    ],
  }),
  methods: {
    countSliderUp() {
      if (this.sliderCount === 2) {
        console.log(1);
        this.sliderCount = 0;
      } else {
        console.log(1 + "no");
        this.sliderCount += 1;
      }
    },
    countSliderDown() {
      if (this.sliderCount <= 0) {
        return;
      } else {
        this.sliderCount -= 1;
      }
    },
  },
  components: {},
  mounted() {
    console.log(this.sliders[this.sliderCount].img);
  },
};
</script>

<style scoped>
button {
  border: none;
  background: none;
}

a {
  text-decoration: none;
}

.wrapper {
  margin-bottom: 4.5%;
  margin-top: 2.5%;
  overflow: hidden;
  transition: width 2s, height 2s, background-color 2s, transform 2s;
}

.slider {
  display: flex;
  align-items: center;

  transition: ease-in 0.5s;

  flex-wrap: wrap;

  justify-content: space-between;

  border-radius: 10px;

  max-width: 1128px;

  margin: 0 auto;

  padding: 30px 36px;
}

.offer__h1 {
  color: black;
}

.slider__offer {
  width: 30%;
}

.offer__a {
  display: inline-block;

  background: #10b648;
  border-radius: 10px;

  padding: 4% 6%;

  color: white;

  border: none;
}

.slider__count {
  display: flex;
  flex-direction: row;

  margin: 0 auto;
}

.slider__breake {
  flex-basis: 100%;
}

.eclipse {
  width: 12px;
  height: 12px;

  margin-right: 10px;

  border-radius: 50%;
  background: rgba(32, 32, 32, 0.31);
}

.eclipse1_,
.eclipse2_,
.eclipse3_ {
  background: #202020;
}

.sliderLeaveLeft {
  transform: translate(-100%, 0px);
}

@media (max-width: 1200px) {
  .slider {
    max-width: 916px;
  }
}

@media (max-width: 916px) {
  .slider {
    max-width: 730px;
  }
}
</style>
