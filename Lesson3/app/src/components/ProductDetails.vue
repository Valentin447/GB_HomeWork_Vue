<template>
  <div class="product">
    <h4 class="name">
      {{ product.name }}
    </h4>
    <p>Price: {{ formattedPrice }}</p>
    <p v-if="product.available">Available</p>
    <p v-else>Out of stock</p>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        product:{
          name: "pen",
          price: 99.99,
          available: true,
        },
      }
    },
    computed:{
      formattedPrice(){
        return `$${this.product.price}`;
      },
    }
  }
</script>

<style lang="scss" scoped>

</style>