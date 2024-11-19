<script setup>
import AppMenu from "@/components/AppMenu.vue";

import { RouterView } from "vue-router";
</script>

<template>
  <div class="root">
    <div class="menuInner">
      <AppMenu />
    </div>
    <main class="main">
      <header class="header">
        <div class="title">
          <slot name="title"></slot>
        </div>
        <div class="controls">
          <slot name="controls"></slot>
        </div>
      </header>
    </main>
  </div>
</template>

<style lang="sass" scoped>
.main
    width: 100%
    padding: 16px
.root
    display: flex
.menuInner
    width: 70px
.header
    display: flex
    justify-content: space-between
    align-items: center
.title
    font-size: 24px
    font-weight: bold
    font-family: sans-serif
    color: violet
</style>
