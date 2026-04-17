<template>
  <div>
    <h1>Favourites</h1>
    <div class="product-grid">
      <ProductCard v-for="product in productsStore.products" :key="product.id" :product="product" />
    </div>
  </div>
</template>

<script>
import { useProductsStore } from '../stores/products'
import ProductCard from '../components/ProductCard.vue'

export default {
  components: { ProductCard },
  computed: {
    productsStore() { return useProductsStore() }
  }
}
</script>