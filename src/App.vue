<template>
<div>

  <PropCard>
    <template v-slot:default="{isInputDisabledSlot}">
      <PropForm :isInputDisabledSlot="isInputDisabledSlot">
        <template v-slot:default="{isInputDisabledSlot}">
          <PropInput :isInputDisabledSlot="isInputDisabledSlot" />
        </template>
      </PropForm>
    </template>
  </PropCard>

  <InjectCard>
    <InjectForm>
      <InjectInput/>
    </InjectForm>
  </InjectCard>

</div>

</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

import InjectCard from './components/inject/InjectCard.vue';
import InjectForm from './components/inject/InjectForm.vue';
import InjectInput from './components/inject/InjectInput.vue';

import PropCard from './components/props/PropCard.vue';
import PropForm from './components/props/PropForm.vue';
import PropInput from './components/props/PropInput.vue';


@Component({
  components: {
    InjectCard,
    InjectForm,
    InjectInput,
    PropCard,
    PropForm,
    PropInput
  },
})
export default class App extends Vue {}
</script>

<style>
body {
  color: white;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  margin-top: 60px;
}
</style>
