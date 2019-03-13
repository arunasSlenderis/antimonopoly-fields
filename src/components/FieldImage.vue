<template>
  <img :src="image" alt="No image available" />
</template>

<script>
export default {
  name: 'FieldImage',

  props: {
    image: { type: String, required: true }
  }
};
</script>

<style scoped lang="scss">
  img {
    max-width: 100%;
  }
</style>
