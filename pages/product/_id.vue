<template>
  <div v-if="product">
    <div class="flex flex-wrap lg:flex-nowrap lg:py-10 py-5 lg:px-20 px-10">
      <!-- Right -->
      <div class="flex-grow">
        <h1 class="text-2xl lg:text-4xl font-bold text-[#30180d] mb-4">
          {{ product.name }}
        </h1>

        <div class="mb-2 lg:hidden">
          <img :src="product.src" class="max-h-[300px]" />
        </div>

        <p class="pl-10">
          {{ product.brief }}
        </p>

        <div>
          <span class="inline-block h-1 w-8 bg-[#bf692d]"></span>
          <span class="inline-block h-1 w-8 bg-[#bf692d]"></span>
          <span class="inline-block h-1 w-8 bg-[#bf692d]"></span>
        </div>

        <br />

        <div v-if="product.benefits && product.benefits.length > 0">
          <h2 class="text-slate-600 text-lg font-semibold">الـفـوائـد:</h2>
          <LI v-for="(benefit, $index) in product.benefits" :key="$index">
            {{ benefit }}
          </LI>
        </div>

        <br />

        <div>
          <nuxt-link
            to="/#contactus"
            class="bg-teal-500 text-white inline-block px-6 py-2 rounded-lg"
          >
            اطلب المنتج
          </nuxt-link>
        </div>
      </div>

      <!-- Left -->
      <div class="w-2/5 hidden lg:block">
        <img :src="product.src" class="max-h-[500px]" />
      </div>
    </div>
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
