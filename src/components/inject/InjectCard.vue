<template>
  <div class="card">
    <h2>Form header</h2>
    <button @click="toggleDisable">disable '{{isInputDisabled.abc}}'</button>
    <slot></slot>
  </div> 
</template>

<script lang="ts">
import { Component, Provide, Vue } from 'vue-property-decorator';

@Component({})
export default class InjectCard extends Vue {

  @Provide('isInputDisabled')
  isInputDisabled = Vue.observable({abc: false})

  toggleDisable() {
    this.isInputDisabled.abc = !this.isInputDisabled.abc
  }


}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card {
  border-radius: 15px;
  background: #2c3e50;
  padding: 20px;
  width: 200px
}

button {
    cursor: pointer;
    margin-bottom: 20px;
    background: #42b883;
    padding: 5px;
    border: none;
    border-radius: 10px;
    color: white;
}

</style>
