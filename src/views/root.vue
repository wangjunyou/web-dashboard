<template>
  <div class="hello">
    hello world {{ msg }}
    <n-button type="primary" @click="cli">cli</n-button>
  </div>
</template>

<script lang="ts" setup>
import {NButton} from 'naive-ui'
import {ref} from "vue";

const msg = ref(1);

const cli = () => {
  console.log('hello');
  msg.value++
}
</script>

<style scoped>
.hello {
  color: red;
}
</style>