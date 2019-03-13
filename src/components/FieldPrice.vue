<template>
  <div class="price">$ {{ price }}</div>
</template>

<script>
export default {
  name: 'FieldPrice',

  props: {
    price: { type: [Number, String], required: true }
  }
};
</script>

<style scoped lang="scss">
.price {
  user-select: none;
}
</style>
