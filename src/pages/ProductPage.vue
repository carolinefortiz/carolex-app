<template>
  <q-page class="bg-pink-1">
    <ProductList :products="products" />
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import ProductList from "components/lists/ProductList.vue";

export default defineComponent({
  name: "ProductPage",
  components: {
    ProductList,
  },
  setup() {
    return {
      products: [
        {
          id: 1,
          name: "Batom Ruby Rose",
          price: 24,
          photo:
            "https://static.cdnlive.com.br/uploads/724/unidade/16926543858831_zoom.jpg",
        },
        {
          id: 2,
          name: "Batom Ruby Rose",
          price: 24.5,
          photo:
            "https://static.cdnlive.com.br/uploads/724/unidade/16926543858831_zoom.jpg",
        },
        {
          id: 3,
          name: "Batom Ruby Rose",
          price: 24.99,
          photo:
            "https://static.cdnlive.com.br/uploads/724/unidade/16926543858831_zoom.jpg",
        },
        {
          id: 4,
          name: "Batom Ruby Rose",
          price: 24.99,
          photo:
            "https://static.cdnlive.com.br/uploads/724/unidade/16926543858831_zoom.jpg",
        },
      ],
    };
  },
});
</script>
