<template>
  <form>
    <slot></slot>
    <button>Send</button>
  </form>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({})
export default class InjectForm extends Vue {}
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
