<template>
  <div>
    <h2>{{ product.name }}</h2>
    <p>{{ formattedPrice }}</p>
    <p>{{ product.available ? "Available" : "Out of stock" }}</p>
  </div>
</template>

<script>
export default {
  name: "ProductDetails",
  props: {},
  data() {
    return {
      product: {
        name: "Название продукта",
        price: 99.99,
        available: true,
      },
    };
  },
  computed: {
    formattedPrice() {
      const price = this.product.price;
      return `$${price.toFixed(2)}`;
    },
  },
};
</script>
<style scoped></style>
