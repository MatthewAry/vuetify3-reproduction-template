<template>
  <VContainer>
    <div>↑ This Tab should be selected</div>
    <div class="text-h1">
      Home Page
    </div>
    <VAlert type="warning" title="Issues">
      <div>
        1. Pressing the back button on the browser to return to this page does not update the active state of the "Home" tab. I even have the exact prop applied.
      </div>
      <div class="pt-3">
        2. <code>VSlideGroup</code> Seems to be throwing a warning in console.
        <pre style="white-space: pre-wrap">
runtime-core.esm-bundler.js:40 [Vue warn]: Maximum recursive updates exceeded in component &#60;VSlideGroup	&#62;. This means you have a reactive effect that is mutating its own dependencies and thus recursively triggering itself. Possible sources include component template, render function, updated hook or watcher source function.
        </pre>
      </div>
    </VAlert>

    <pre>
const routes = [
  {
    path: '/',
    component: () => import('@/layouts/default/Default.vue'),
    children: [
      {
        path: '',
        name: 'Home',
        component: () => import('@/views/Home.vue'),
      },
     ...
    ],
  },
]
    </pre>
  </VContainer>
</template>

<script lang="ts" setup>

</script>
