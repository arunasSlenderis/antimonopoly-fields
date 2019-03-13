<template>
  <div>
    <FieldTitle title="Competitor or Monopolist" />
    <FieldImage class="image-container" :image="image" />
  </div>
</template>

<script>
import FieldTitle from '@/components/FieldTitle';
import FieldImage from '@/components/FieldImage';
import actionImage from '@/assets/actionImage.png';

export default {
  name: 'ActionField',

  components: {
    FieldTitle,
    FieldImage
  },

  computed: {
    image() {
      return actionImage;
    }
  }
};
</script>

<style scoped lang="scss">
.image-container {
  margin: 20px 0 20px 0;
  width: 80%;
}
</style>
