<template>
  <div id="app">
    <FieldContainer class="field-container">
      <!--<CityPartField/>-->
      <!--<ActionField />-->
      <!--<CompanyField />-->
      <TaxField />
    </FieldContainer>
  </div>
</template>

<script>
import FieldContainer from '@/components/FieldContainer';
import CityPartField from '@/components/CityPartField';
import ActionField from '@/components/ActionField';
import CompanyField from '@/components/CompanyField';
import TaxField from '@/components/TaxField';

export default {
  name: 'app',

  components: {
    TaxField,
    ActionField,
    FieldContainer,
    CityPartField,
    CompanyField
  }
};
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;

  .field-container {
    display: inline-block;
    width: 200px;
  }
}
</style>
