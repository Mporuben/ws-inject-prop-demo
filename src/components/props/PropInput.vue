<template>
  <div>
    <label>Test</label> <br/>
    <input :disabled="isInputDisabledSlot"/> 
  </div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator';

@Component({})
export default class PropInput extends Vue {

  @Prop(Boolean)
  isInputDisabledSlot!: boolean

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div {
    text-align: left;
}
input {
    width: 100%;
    padding: 5px;
    border: none;
    border-radius: 5px;
}
label{
    color: white
}

</style>
