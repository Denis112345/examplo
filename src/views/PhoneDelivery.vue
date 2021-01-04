<template>
  <div class="header">
    <div class="header__container">
      <div class="header__delivery">
        <img
          height="15px"
          width="15px"
          class="header__clockImg"
          src="@/img/clock.png"
          alt="clock"
        />
        Доставка с 8:30 до 22:30
      </div>

      <div class="header__phoneNumber">
        <img
          height="15px"
          width="15px"
          class="header__callImg"
          src="@/img/Call.png"
          alt="Call"
        />
        + 8 800-300-8414
      </div>
    </div>
  </div>
</template>

<style scoped>
.header {
  margin-bottom: 19px;

  background: #3f403e;
  padding: 2px;
  line-height: 6%;
}

.header__container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
}

.header__delivery,
.header__phoneNumber {
  display: inline-flex;
  align-items: center;

  white-space: nowrap;
}

.header__clockImg {
  width: 15, 83px;
  height: 15, 83px;
  margin-right: 7px;

  align-self: center;
}

@media (max-width: 1200px) {
  .header__container {
    max-width: 916px;
  }
}

@media (max-width: 916px) {
  .header__container {
    max-width: 730px;
  }
}

@media (max-width: 767px) {
  .header__container {
    max-width: none;
  }
}
</style>
