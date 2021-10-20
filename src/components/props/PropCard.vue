<template>
  <div class="card">
    <h2>Form header</h2>
    <button @click="toggleDisable">disable '{{isInputDisabledSlot}}'</button>
    <slot :isInputDisabledSlot="isInputDisabledSlot"></slot>
  </div> 
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({})
export default class PropCard extends Vue {


  isInputDisabledSlot = false

  toggleDisable() {
    this.isInputDisabledSlot = !this.isInputDisabledSlot
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
