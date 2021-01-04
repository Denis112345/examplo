<template>
  <div class="blockBenefits">
    <ItemBlockBenefits :infoFromBlock="infoFromBlock[0]" />
    <ItemBlockBenefits :infoFromBlock="infoFromBlock[1]" />
    <ItemBlockBenefits :infoFromBlock="infoFromBlock[2]" />
  </div>
</template>

<script>
import ItemBlockBenefits from "@/views/ItemBlockBenefits";

export default {
  components: {
    ItemBlockBenefits,
  },
  data: () => ({
    infoFromBlock: [
      {
        id: 1,
        img: "icon1.png",
        title: "Всегда свежая и натуральная продукция",
      },
      {
        id: 2,
        img: "icon2.png",
        title: "Доставка в удобное для вас время",
      },
      {
        id: 3,
        img: "icon3.png",
        title: "Выгодные цены и скидки постоянным клиентам",
      },
    ],
  }),
  mounted() {
    console.log(this.infoForBlockBenefits);
  },
};
</script>

<style scoped>
.blockBenefits {
  display: flex;
  max-width: 1200px;
  margin: 0 auto;
}

.blockBenefits > .wrapper {
  margin-right: 3%;

  width: 33%;
}

.blockBenefits > .wrapper:last-child {
  margin-right: 0;
}
</style>
