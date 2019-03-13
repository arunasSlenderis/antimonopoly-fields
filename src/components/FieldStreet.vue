<template>
  <div class="street-name">{{ streetName }}</div>
</template>

<script>
export default {
  name: 'FieldStreet',

  props: {
    streetName: { type: String, required: true }
  }
};
</script>

<style scoped lang="scss">
.street-name {
  user-select: none;
}
</style>
