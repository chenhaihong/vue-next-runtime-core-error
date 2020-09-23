<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
<pre>
  <!-- <code class="javascript" v-hljs>const a = 100;</code> -->
  <code class="javascript">const a = 100;</code>
</pre>
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src

export default defineComponent({
  name: 'Home',
  components: {
    HelloWorld,
  },
});
</script>
