<template>
  <VMain>
    <VTabs>
      <VTab :to="{ name: 'Home' }" :exact="true">Home</VTab>
      <VTab :to="{ name: 'one' }">Page 1</VTab>
      <VTab :to="{ name: 'two' }">Page 2</VTab>
    </VTabs>
    <RouterView />
  </VMain>
</template>

<script lang="ts" setup>
  //
</script>

<style scoped>
  .v-tab--selected {
    background-color: #eaeaea;
  }
</style>
