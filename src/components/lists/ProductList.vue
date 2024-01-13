<template>
  <div class="row q-pa-xs">
    <div class="col-lg-2 q-pa-xs" v-for="product of products" :key="product.id">
      <q-card>
        <img :src="product.photo" />

        <q-card-section>
          <div class="text-body2 text-uppercase">
            {{ product.name }}
          </div>
        </q-card-section>

        <q-card-section>
          <div class="text-subtitle2 row justify-between items-center">
            R$ {{ product.price }}
            <q-btn color="primary" icon="add_shopping_cart" round flat />
          </div>
        </q-card-section>
      </q-card>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductList",
  props: {
    products: {
      type: Array,
      required: true,
    },
  },
};
</script>
