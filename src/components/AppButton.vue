<script setup>
const props = defineProps({
  text: {
    type: String,
    default: "",
  },
});
</script>

<template>
  <el-button class="btn" type="primary">
    {{ text }}
  </el-button>
</template>

<style lang="sass" scoped>
.btn
    background-color: violet
    border: none
    padding: 20px 20px
</style>
