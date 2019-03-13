<template>
  <div>
    <FieldTitle title="Income Tax" />
    <FieldDescription class="field-description" :description="description" />
  </div>
</template>

<script>
import FieldTitle from '@/components/FieldTitle';
import FieldDescription from '@/components/FieldDescription';

export default {
  name: 'TaxField',

  components: {
    FieldTitle,
    FieldDescription
  },

  data() {
    return {
      description: 'Pay $200 or a percentage of your assets'
    };
  }
};
</script>

<style scoped lang="scss">
.field-description {
  margin-top: 60px;
}
</style>
