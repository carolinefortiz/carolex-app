<template>
  <q-page class="bg-pink-1">
    <OrderList :orders="orders" />
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import OrderList from "components/lists/OrderList.vue";

export default defineComponent({
  name: "OrderPage",
  components: {
    OrderList,
  },
  setup() {
    return {
      orders: [
        {
          id: 1,
          client: "Romilda Souza",
          totalProducts: 24,
          totalPrice: 500,
        },
        {
          id: 2,
          client: "Ramona Rech",
          totalProducts: 3,
          totalPrice: 170,
        },
        {
          id: 3,
          client: "Wally Silva",
          totalProducts: 14,
          totalPrice: 223,
        },
        {
          id: 4,
          client: "Tulipa Guina",
          totalProducts: 66,
          totalPrice: 666,
        },
      ],
    };
  },
});
</script>
