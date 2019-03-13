<template>
  <div class="field-monopolists-houses" :style="{ background }">
    M
  </div>
</template>

<script>
export default {
  name: 'MonopolistsHousesPlace',

  props: {
    background: { type: String, required: true }
  }
};
</script>

<style scoped lang="scss">
.field-monopolists-houses {
  padding: 10px;
  font-size: 26px;
  user-select: none;
  overflow: hidden;
  max-height: 40px;
  border-bottom: 3px solid;
  border-left: 3px solid;
  border-right: 3px solid;
}
</style>
