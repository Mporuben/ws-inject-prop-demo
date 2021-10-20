<template>
  <form>
    <slot :isInputDisabledSlot="isInputDisabledSlot"></slot>

    <button>Send</button>
  </form>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component({})
export default class PropForm extends Vue {
  @Prop(Boolean)
  isInputDisabledSlot!: boolean
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
button {
    cursor: pointer;
    margin-top: 20px;
    background: #42b883;
    padding: 10px;
    font-size: 1.1em;
    border: none;
    border-radius: 10px;
    color: white;
}
</style>
