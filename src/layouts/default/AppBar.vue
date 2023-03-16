<template>
  <v-app-bar flat>
    <v-app-bar-title>
      <v-icon icon="mdi-circle-slice-6" />

      Essentials Preset
    </v-app-bar-title>
    <VBtn v-if="router.currentRoute.value.name !== 'Home'" @click="router.back()">Click Me Till You Get Home</VBtn>
    <VChip :color="home.isExactActive.value ? 'green' : 'red'">Home {{ home.isActive.value ? 'Active' : 'Inactive' }}</VChip>
    <VChip :color="page1.isExactActive.value ? 'green' : 'red'">Page 1 {{ page1.isActive.value ? 'Active' : 'Inactive' }}</VChip>
    <VChip :color="page2.isExactActive.value ? 'green' : 'red'">Page 2 {{ page2.isActive.value ? 'Active' : 'Inactive' }}</VChip>
  </v-app-bar>
</template>

<script lang="ts" setup>
  import { useRouter } from 'vue-router'

  const router = useRouter()
  import { useLink } from 'vue-router'

  const home = useLink({ to: { name: 'Home' }})
  const page1 = useLink({ to: { name: 'one' }})
  const page2 = useLink({ to: { name: 'two' }})
</script>
