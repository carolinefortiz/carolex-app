<template>
  <div class="q-pa-sm">
    <q-table
      title="Pedidos"
      :columns="formatHeaders(headers)"
      :rows="orders"
      row-key="id"
    />
  </div>
</template>

<script>
import { formatToBRL } from "brazilian-values";

export default {
  name: "OrderList",
  props: {
    orders: {
      type: Array,
      required: true,
    },
  },
  setup() {
    return {
      headers: {
        id: "ID",
        client: "Nome do cliente",
        totalProducts: "Quantidade de produtos",
        totalPrice: "Total",
      },
    };
  },
  methods: {
    formatHeaders(headers) {
      return Object.keys(headers).map((key) => {
        return {
          name: key,
          field: key,
          align: "left",
          sortable: true,
          required: true,
          label: headers[key],
          format: (val, row) => {
            if (val === row.totalPrice) return formatToBRL(val);
            return val;
          },
        };
      });
    },
  },
};
</script>
