<script setup lang="ts">

</script>

<template>
  <VContainer>
    Page 2
    <pre>
const routes = [
  {
    path: '/',
    component: () => import('@/layouts/default/Default.vue'),
    children: [
      ...
      {
        path: 'page2',
        name: 'two',
        component: () => import('@/views/Page2.vue'),
      },
    ],
  },
]
    </pre>
  </VContainer>
</template>
