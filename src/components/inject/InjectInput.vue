<template>
  <div>
    <label>Test</label> <br/>
    <buton @click="isInputDisabled.abc =  !isInputDisabled.abc">test</buton>
    <input :disabled="isInputDisabled.abc"/>
  </div>
</template>

<script lang="ts">
import { Component, Inject, Vue } from 'vue-property-decorator';

@Component({})
export default class InjectInput extends Vue {

  @Inject('isInputDisabled')
  isInputDisabled!: boolean

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
