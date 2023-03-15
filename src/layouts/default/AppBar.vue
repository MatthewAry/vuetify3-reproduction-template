<template>
  <v-app-bar flat>
    <v-app-bar-title>
      <v-icon icon="mdi-circle-slice-6" />

      Essentials Preset
    </v-app-bar-title>
    <VBtn v-if="router.currentRoute.value.name !== 'Home'" @click="router.back()">Click Me Till You Get Home</VBtn>
  </v-app-bar>
</template>

<script lang="ts" setup>
  import { useRouter } from 'vue-router'

  const router = useRouter()
</script>
