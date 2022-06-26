<template>
  <h1>{{ msg }}</h1>

  <p>
    Recommended IDE setup:
    <a href="https://code.visualstudio.com/" target="_blank">VS Code</a>
    +
    <a href="https://github.com/johnsoncodehk/volar" target="_blank">Volar</a>
  </p>

  <p>See <code>README.md</code> for more information.</p>

  <p>
    <a href="https://vitejs.dev/guide/features.html" target="_blank">
      Vite Docs
    </a>
    |
    <a href="https://v3.vuejs.org/" target="_blank">Vue 3 Docs</a>
  </p>

  <p>{{ totals }}</p>
  <button type="button" @click="counts">count is: {{ count }}</button>
  &nbsp;
  <n-button type="primary" @click="counts">count is: {{ count }}</n-button>
  <!--  <button type="button" @click=""-->
  <p>
    Edit
    <code>components/HelloWorld.vue</code> to test hot module replacement.
  </p>
</template>

<script lang="ts">
  import { defineComponent, ref } from 'vue'
  import { NButton } from 'naive-ui'

  export default defineComponent({
    name: 'HelloWorld',
    components: {
      NButton
    },
    props: {
      msg: {
        type: String,
        default: {}
      }
    },
    setup() {
      const count = ref(0)
      return { count }
    },
    data() {
      return {
        totals: 0
      }
    },
    methods: {
      counts() {
        // console.log(this.count + "==" + this.msg + "==" + this.totals);
        this.count++
        this.totals++
      }
    }
  })
</script>

<style scoped>
  a {
    color: #42b983;
  }

  label {
    margin: 0 0.5em;
    font-weight: bold;
  }

  code {
    background-color: #eee;
    padding: 2px 4px;
    border-radius: 4px;
    color: #304455;
  }
</style>
