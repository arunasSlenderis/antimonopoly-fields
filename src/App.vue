<template>
  <div id="app">
    <transition name="fade">
      <FieldContainer class="container" v-if="appear">
        <TaxField />
      </FieldContainer>
    </transition>
    <br />
    <br />
    <button @click="appear = !appear">Toggle</button>
  </div>
</template>

<script>
import FieldContainer from '@/components/FieldContainer';
import TaxField from '@/components/TaxField';

export default {
  name: 'app',

  components: {
    TaxField,
    FieldContainer
  },

  data() {
    return {
      appear: false
    };
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

  .container {
    display: inline-block;
    width: 200px;
  }

  .fade-enter-active,
  .fade-leave-active {
    transition: all 0.5s ease-in-out;
  }
  .fade-enter,
  .fade-leave-to {
    opacity: 0;
  }

  .fade-enter {
    transform: translateX(200px);
  }
  .fade-leave-to {
    transform: translateX(-200px);
  }
}
</style>
