<template>
  <Sidebar />
  <main>
    <div class="flex justify-between ml-[250px]">
      <slot />
      <RightSidebar />
    </div>
  </main>
</template>

<script setup></script>

<style lang="scss" scoped></style>
