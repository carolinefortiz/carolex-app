<template>
  <q-input v-model="name" label="Nome" />
</template>

<script>
import { defineComponent } from "vue";
import { ref } from "vue";

export default defineComponent({
  name: "ProductForm",
  setup() {
    return {
      name: ref(""),
    };
  },
});
</script>
