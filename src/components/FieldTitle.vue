<template>
  <div class="title">{{ title }}</div>
</template>

<script>
export default {
  name: 'FieldTitle',

  props: {
    title: { type: String, required: true }
  }
};
</script>

<style scoped lang="scss">
.title {
  text-align: center;
  font-size: 1.2rem;
  font-weight: bold;
}
</style>
