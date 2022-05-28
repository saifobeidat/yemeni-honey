<template>
  <div class="flex flex-wrap">
    <div
      v-for="(item, $index) in products"
      :key="$index"
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
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      products: [
        {
          src: "/products/3ood_abyad_malaki.jpg",
          name: "العود الأبيض اليمني",
        },
        {
          src: "/products/sedir_do3ni.jpg",
          name: "السدر الدوعني",
        },
        {
          src: "/products/3saimy_malaki.jpg",
          name: "عسل السدر العصيمي الملكي",
        },
        {
          src: "/products/sedir_jabali.jpg",
          name: "عسل السدر الجبلي",
        },
        {
          src: "/products/sedir_rabe3i.jpg",
          name: "عسل السدر الربيعي",
        },
        {
          src: "/products/samar_hadrami_malaki.jpg",
          name: "عسل السمر الحضرمي الملكي",
        },
        {
          src: "/products/azhar_jabali.jpg",
          name: "عسل الازهار الجبلي",
        },
        {
          src: "/products/sham3_3asal.jpg",
          name: "شمع العسل (الشهد)",
        },
        {
          src: "/products/sedir_gerfeh.jpg",
          name: "عسل السدر بالقرفه",
        },
        {
          src: "/products/with_zangabel.jpg",
          name: "العسل بالزنجبيل",
        },
        {
          src: "/products/b_ghedaa_malikat_w_a3haab.jpg",
          name: "العسل بغذاء الملكات والاعشاب",
        },
        {
          src: "/products/saal_7araq.jpg",
          name: "عسل الصال الحراق",
        },
        {
          src: "/products/with_3akbar.jpg",
          name: "العسل بالعكبر ( البروبليس)",
        },
      ],
    };
  },
};
</script>

<style></style>
