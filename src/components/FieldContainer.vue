<template>
  <div class="field-container"><slot /></div>
</template>

<script>
export default {
  name: 'FieldContainer'
};
</script>

<style scoped lang="scss">
.field-container {
  border: 2px solid;
}
</style>
