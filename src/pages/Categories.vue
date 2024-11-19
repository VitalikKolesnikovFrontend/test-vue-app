<script setup>
import AppButton from "@/components/AppButton.vue";
import AppLayout from "@/layouts/AppLayout.vue";
</script>

<template>
  <AppLayout>
    <template #title>Categories</template>
    <template #controls>
      <AppButton text="Add categories" />
    </template>
    <template #inner></template>
  </AppLayout>
</template>
