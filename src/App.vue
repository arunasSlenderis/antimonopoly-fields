<template>
  <div id="app">
    <transition-group name="fade">
      <template v-for="field in fields">
        <FieldContainer
          v-if="!field.hidden"
          :key="field.title"
          class="container"
        >
          <TaxField :title="field.title" />
        </FieldContainer>
      </template>
    </transition-group>
    <br />
    <br />
    <button @click="nextField">Toggle</button>
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
      fields: [
        { title: 'Field 1', hidden: false },
        { title: 'Field 2', hidden: true },
        { title: 'Field 3', hidden: true }
      ],
      visibleFieldIndex: null
    };
  },

  methods: {
    nextField() {
      this.fields = this.fields.map((field, index, fieldsArray) => {
        if (!field.hidden) {
          if (index === fieldsArray.length - 1) {
            this.visibleFieldIndex = 0;
          } else {
            this.visibleFieldIndex = index + 1;
          }
        }
        if (this.visibleFieldIndex === index)
          return { ...field, hidden: false };

        return { ...field, hidden: true };
      });
    }
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
  .fade-enter-to {
    transform: translateX(-100px);
  }
  .fade-leave-to {
    transform: translateX(-200px);
  }
}
</style>
