<template>
  <q-page class="flex flex-center">
    <ProductForm />
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import ProductForm from "components/forms/ProductForm.vue";

export default defineComponent({
  name: "ProductPage",
  components: {
    ProductForm,
  },
});
</script>
