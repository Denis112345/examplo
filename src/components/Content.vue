<template>
  <div class="content">
    <Slider />
    <BlockBenefits />
  </div>
</template>

<script>
import Slider from "@/views/Slider";
import BlockBenefits from "@/views/BlockBenefits";

export default {
  components: {
    Slider,
    BlockBenefits,
  },
};
</script>

<style scoped>
.content {
  margin: 0 auto;
}

@media (max-width: 1200px) {
  .content {
    max-width: 916px;
  }
}

@media (max-width: 916px) {
  .content {
    max-width: 730px;
  }
}

@media (max-width: 767px) {
  .content {
    max-width: none;
  }
}
</style>
