<template>
  <div>
    {{ message }}
    <button @click="logMessage">Log Message</button>
  </div>
</template>

<script>
export default {
  mounted() {
    console.log('Hello World');
  }
};
</script>