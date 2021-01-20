<template>
  <h2>{{ text.value }}</h2>
  <h2>Total Length - {{ listLength }}</h2>
</template>

<script>
export default {
  inject:["text","listLength"],
};
</script>