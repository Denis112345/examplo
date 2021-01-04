<template>
  <div class="wrapper">
    <img :src="require(`@/img/${infoFromBlock.img}`)" />
    {{ infoFromBlock.title }}
  </div>
</template>

<script>
export default {
  props: ["infoFromBlock"],
};
</script>

<style scoped>
.wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 25px 30px;

  color: black;
  font-weight: 600;

  border-radius: 12px;
  border: 1px solid #ebebeb;
}
</style>
