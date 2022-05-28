<template>
  <div>
    <Header />

    <div class="flex">
      <section class="text-center w-1/3 flex-shrink-0">
        <!-- Logo -->
        <img class="w-auto md:w-56 lg:w-80 mx-auto" src="/logo.jpg" />

        <!-- Slogan -->
        <div
          class="text-center font-extrabold text-3xl md:text-4xl lg:text-7xl"
        >
          <h1 class="text-[#b83806]">عـســـل</h1>
          <h1 class="text-[#221e1d]">يـــمــنــي</h1>
          <h1 class="text-[#d87c19]">طبيعي</h1>
        </div>
      </section>

      <!-- Left Section  -->
      <section class="relative z-50 flex flex-grow justify-end">
        <!-- Big Shape  -->
        <img
          src="/shape.jpg"
          class="absolute md:relative -top-8 md:-top-16 -left-16 md:-left-52 rounded-[60%] select-none"
        />

        <!-- Flower -->
        <img src="/flower.png" class="absolute top-0 left-0 w-20 md:w-auto" />

        <!-- Honey -->
        <img
          src="/honey.png"
          class="absolute moving-animation top-1/4 right-0 w-44 md:w-72 lg:w-[450px]"
        />
      </section>
    </div>

    <div id="products" class="bg-orange-100 section-padding">
      <SectionTitle> المنتجات </SectionTitle>
      <Products />
    </div>
    <div id="contactus" class="section-padding">
      <SectionTitle> تواصل معنا </SectionTitle>
      <div class="mb-10">
        خيرات الجنتين للعسل اليمني الشركة الرائده في عالم العسل اليمني والمنتجات
        اليمنية الطبيعية تأسست عام 1975م نتميز بتوفير اجود انواع العسل اليمني من
        كل مناطق اليمن الجبلية اشهرها عسل السدر العصيمي الملكي والسدر الدوعني
        والسدر الجبلي الجرداني سدر شبوه عسل السدر المأربي والسدر الوصابي والسدر
        الجوفي والعسل السقطري وعسل السمر الحضرمي وعسل الصال الحراق وعسل الازهار
        الجبلي نوفر اجود انواع البُن اليمني (القهوة ) بانواعها والقشر اليمني
        والحناء اليمنية وكل انواع البخور اليمني .
      </div>
      <div class="flex justify-center">
        <div class="inline-flex bg-slate-100 p-5 shadow-md">
          <div>
            <div class="mb-2">
              <div class="font-medium">الجمهورية اليمنية</div>
              <div class="flex">
                <div>صنعاء شارع المطار:</div>
                <div class="mr-2">00967776002009</div>
              </div>
            </div>

            <div>
              <div class="font-medium">المملكة الاردنية الهاشمية</div>
              <div class="flex">
                <div>مكه مول الطابق الاول:</div>
                <div class="mr-2">0792507555</div>
              </div>
              <div class="flex">
                <div>افينيو مول:</div>
                <div class="mr-2">0788363670</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
};
</script>

<style scoped>
.section-padding {
  @apply px-10 py-8 lg:px-20 lg:py-16;
}
.moving-animation {
  animation: bounce 4s linear infinite;
}

@keyframes bounce {
  0% {
    transform: translate3d(0px, 0px, 0);
  }

  50% {
    transform: translate3d(-10px, -10px, 0);
  }
  100% {
    transform: translate3d(0px, 0px, 0);
  }
}
</style>
