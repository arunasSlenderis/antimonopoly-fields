<template>
  <div>{{ description }}</div>
</template>

<script>
export default {
  name: 'FieldDescription',

  props: {
    description: { type: String, required: true }
  }
};
</script>

<style scoped></style>
