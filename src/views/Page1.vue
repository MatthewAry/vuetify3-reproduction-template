<script setup lang="ts">

</script>

<template>
  <VContainer>
    Page 1
    <pre>
const routes = [
  {
    path: '/',
    component: () => import('@/layouts/default/Default.vue'),
    children: [
      ...
      {
        path: 'page1',
        name: 'one',
        component: () => import('@/views/Page1.vue'),
      },
      ...
    ],
  },
]
    </pre>
  </VContainer>
</template>
