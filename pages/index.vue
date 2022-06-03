<template>
  <div>
    <div class="flex min-h-[250px]">
      <section class="text-center w-1/3 flex-shrink-0">
        <!-- Logo -->
        <img
          class="hidden sm:inline-block md:w-56 lg:w-60 mx-auto mt-3"
          src="/logo.png"
        />

        <!-- Slogan -->
        <div
          class="text-center font-extrabold text-2xl sm:text-3xl md:text-4xl lg:text-6xl mt-8 sm:mt-0"
        >
          <h1 class="text-[#b83806]">خيرات الجنتين</h1>
          <h1 class="text-[#221e1d]">للعسل</h1>
          <h1 class="text-[#d87c19]">اليمني</h1>
        </div>
      </section>

      <!-- Left Section  -->
      <section class="relative z-50 flex flex-grow justify-end">
        <!-- Big Shape  -->
        <img
          src="/shape.jpg"
          class="absolute md:relative -top-8 md:-top-36 -left-16 md:-left-52 rounded-[60%] select-none"
        />

        <!-- Flower -->
        <img src="/flower.png" class="absolute top-0 left-0 w-20 md:w-auto" />

        <!-- Honey -->
        <img
          src="/honey.png"
          class="absolute moving-animation top-[20%] right-0 w-44 md:w-72 lg:w-[450px]"
        />
      </section>
    </div>

    <div id="products" class="bg-orange-100 section-padding">
      <SectionTitle> المنتجات </SectionTitle>
      <div class="flex flex-wrap">
        <nuxt-link
          v-for="(item, $index) in products"
          :key="$index"
          :to="`/product/${item.slug}`"
          class="bg-[#f4eae1] my-4 sm:mx-3 sm:w-[calc(50%-24px)] md:mx-3 md:w-[calc(33.333%-24px)] xl:mx-4 xl:w-[calc(25%-32px)]"
        >
          <div class="h-[calc(100%-60px)]">
            <img
              :src="item.src"
              class="block object-cover object-center w-full h-full"
            />
          </div>
          <div class="font-extrabold text-lg p-4 text-[#6b331a]">
            {{ item.name }}
          </div>
        </nuxt-link>
      </div>
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
              <div class="flex flex-wrap">
                <div class="w-full sm:w-auto">صنعاء شارع المطار:</div>
                <div class="sm:mr-2">00967776002009</div>
              </div>
            </div>

            <div>
              <div class="font-medium">المملكة الاردنية الهاشمية</div>
              <div class="flex flex-wrap mb-2">
                <div class="w-full sm:w-auto">مكه مول الطابق الاول:</div>
                <div class="sm:mr-2">0792507555</div>
              </div>
              <div class="flex flex-wrap mb-2">
                <div class="w-full sm:w-auto">افينيو مول:</div>
                <div class="sm:mr-2">0788363670</div>
              </div>
              <div class="flex flex-wrap mb-2">
                <!-- ## -->
                <div class="w-full sm:w-auto">
                  الجاردنز مقابل مطعم. السروات:
                </div>
                <div class="sm:mr-2">0798120099</div>
              </div>

              <div>
                <div class="font-medium">الايميل</div>
                <div class="flex flex-wrap mb-2">
                  <div class="w-full sm:w-auto">yemenhoneyk@gmail.com</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { mapState } from "vuex";
export default {
  name: "IndexPage",
  computed: {
    ...mapState("products", ["products"]),
  },
};
</script>

<style scoped>
.section-padding {
  @apply px-8 py-8 lg:px-20 lg:py-16;
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
