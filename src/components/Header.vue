<template>
  <div>
    <PhoneDelivery />
    <HeaderSerch />
  </div>
</template>

<script>
import HeaderSerch from "@/views/HeaderSerch";
import PhoneDelivery from "@/views/PhoneDelivery";

export default {
  name: "Header",
  components: { HeaderSerch, PhoneDelivery },
};
</script>
