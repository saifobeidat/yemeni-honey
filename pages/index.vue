<template>
  <div>
    <!-- <Header /> -->
    <div class="flex">
      <section class="text-center w-1/3">
        <!-- Links -->
        <nav class="py-5 font-medium text-lg">
          <a href="#products" class="mx-2 hover:text-blue-500"> المنتجات</a>
          <a href="#contactus" class="mx-2 hover:text-blue-500"> تواصل معنا</a>
        </nav>
        <!-- Logo -->
        <img class="max-w-xs mx-auto" src="/logo.jpg" />

        <!-- Slogan -->
        <div class="text-center font-extrabold text-7xl">
          <h1 class="text-[#b83806]">عـســـل</h1>
          <h1 class="text-[#221e1d]">يـــمــنــي</h1>
          <h1 class="text-[#d87c19]">طبيعي</h1>
        </div>
      </section>

      <!-- Left Section  -->
      <section class="relative flex flex-grow justify-end">
        <!-- Big Shape  -->
        <img src="/shape.jpg" class="relative -top-16 rounded-[60%] -left-52" />

        <!-- Flower -->
        <img src="/flower.png" class="absolute top-0 left-0" />

        <!-- Honey -->
        <img src="/honey.png" class="absolute top-1/4 right-0 max-w-md" />
      </section>
    </div>

    <div id="products" class="min-h-[500px]">Products</div>
    <div id="contactus" class="min-h-[500px]">Contact Us</div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
};
</script>
