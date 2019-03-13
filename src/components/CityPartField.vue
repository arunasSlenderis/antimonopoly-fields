<template>
  <div class="city-part-container">
    <FieldCity cityName="Los Angeles" background="brown" />

    <MonopolistsHousesPlace
      background="brown"
      class="monopolists-houses-place"
    />

    <div class="container-bottom-part">
      <FieldStreet streetName="Hollywood Blvd." />
      <FieldPrice price="120" />
    </div>
  </div>
</template>

<script>
import FieldCity from '@/components/FieldCity';
import MonopolistsHousesPlace from '@/components/MonopolistsHousesPlace';
import FieldStreet from '@/components/FieldStreet';
import FieldPrice from '@/components/FieldPrice';
export default {
  name: 'CityPartField',

  components: {
    FieldCity,
    MonopolistsHousesPlace,
    FieldStreet,
    FieldPrice
  }
};
</script>

<style scoped lang="scss">
.city-part-container {
  width: 100%;

  .monopolists-houses-place {
    width: 60%;
    margin: 0 auto;
  }

  .container-bottom-part {
    margin: 40px 0 20px 0;
  }
}
</style>
