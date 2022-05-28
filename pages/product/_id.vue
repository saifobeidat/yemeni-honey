<template>
  <div v-if="product">
    {{ product.name }}
  </div>
</template>

<script>
export default {
  data() {
    return {
      product: null,
    };
  },
  async created() {
    this.product = await this.$store.dispatch(
      "products/getProductBySlug",
      this.$route.params.id
    );
  },
};
</script>

<style></style>
