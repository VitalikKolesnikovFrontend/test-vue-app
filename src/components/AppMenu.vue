<script setup>
import { ROUTES_PATH } from "@/constants";
import { onMounted } from "vue";
import { RouterView, useRoute, useRouter } from "vue-router";

const router = useRouter();
const route = useRoute();
const usePathActive = (path) => {
  return route.path === path;
};
onMounted(usePathActive);
</script>

<template>
  <div class="menu">
    <div class="logo">
      <svg
        class="w-6 h-6 text-gray-800 dark:text-white"
        aria-hidden="true"
        xmlns="http://www.w3.org/2000/svg"
        width="60"
        height="60"
        fill="currentColor"
        viewBox="0 0 24 24"
        color="green"
      >
        <path
          d="M14.5 3 12 7.156 9.857 3H2l10 18L22 3h-7.5ZM4.486 4.5h2.4L12 13.8l5.107-9.3h2.4L12 18.021 4.486 4.5Z"
        />
      </svg>
    </div>
    <el-menu :router="true" class="nav">
      <el-menu-item
        :index="ROUTES_PATH.HOME"
        :class="['item', usePathActive(ROUTES_PATH.HOME) && 'active']"
      >
        <el-icon :size="44"><Food /></el-icon>
      </el-menu-item>
      <el-menu-item
        :index="ROUTES_PATH.CATEGORIES"
        :class="['item', usePathActive(ROUTES_PATH.CATEGORIES) && 'active']"
      >
        <el-icon :size="44"><Dish /></el-icon>
      </el-menu-item>
    </el-menu>
  </div>
</template>

<style lang="sass" scoped>
.menu
    height: 100vh
    padding: 20px  0
    border-right: 1px solid lightgrey
.nav
    border: none
.logo
    padding: 0 0 15px
    border-bottom: 1px solid lightgrey
.item
    color: pink

    &.active
        color: violet
</style>
