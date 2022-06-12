<template>
  <!--  <img alt="Vue logo" src="./assets/logo.png"/>-->
  <!--  <HelloWorld msg="Hello Vue 3 + TypeScript + Vite"/>-->
  <n-config-provider>
    <n-message-provider>
      <hello-world msg="Hello Vue 3 + TypeScript + Vite" />
    </n-message-provider>
  </n-config-provider>
</template>

<script lang="ts">
  import { defineComponent } from 'vue'
  import HelloWorld from './components/HelloWorld.vue'
  import { NConfigProvider, NMessageProvider } from 'naive-ui'

  export default defineComponent({
    components: {
      HelloWorld,
      NConfigProvider,
      NMessageProvider
    }
  })
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
