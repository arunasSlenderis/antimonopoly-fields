<template>
  <div class="field-city" :style="{ background }">
    {{ cityName }}
  </div>
</template>

<script>
export default {
  name: 'FieldCity',

  props: {
    cityName: { type: String, required: true },
    background: { type: String, required: true }
  }
};
</script>

<style scoped lang="scss">
.field-city {
  padding: 11px 10px;
  font-weight: bold;
  font-size: 20px;
  user-select: none;
  overflow: hidden;
  line-height: 20px;
  max-height: 40px;
  border-bottom: 3px solid;
}
</style>
