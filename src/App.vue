<script>
import Locomotive from './components/Locomotive.vue';

export default {
  name: "App",
  components: {
    Locomotive
  }
};
</script>

<template>
  <div id="scroll-container">
    <Locomotive />
  </div>
</template>

<style>
#scroll-container {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    min-height: 100vh;
    overflow: auto;
    perspective: 1px;
}
</style>
