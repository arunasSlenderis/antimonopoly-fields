<template>
  <div class="company-field-container">
    <FieldTitle title="U.S. Rail road" />
    <FieldImage class="image-container" :image="image" />
    <FieldPrice price="200" />
  </div>
</template>

<script>
import FieldTitle from '@/components/FieldTitle';
import FieldImage from '@/components/FieldImage';
import FieldPrice from '@/components/FieldPrice';

import trainImage from '@/assets/trainStation.jpeg';
export default {
  name: 'CompanyField',
  components: { FieldPrice, FieldImage, FieldTitle },
  computed: {
    image() {
      return trainImage;
    }
  }
};
</script>

<style scoped lang="scss">
.image-container {
  margin: 40px 0 10px 0;
  width: 50%;
}
</style>
