<script setup>
import { ref } from 'vue'
import NavItem from './NavItem.vue'
import {
  HomeIcon,
  IdentificationIcon,
  ListBulletIcon,
  ChatBubbleLeftIcon,
} from '@heroicons/vue/24/outline'

const navItems = {
  mainPage: HomeIcon,
  postListPage: ListBulletIcon,
  usersListPage: IdentificationIcon,
  commentsPage: ChatBubbleLeftIcon,
}

const currentPage = ref('mainPage')
</script>

<template>
  <nav class="TheNav">
    <ul class="TheNavList">
      <NavItem
        v-for="(icon, page) in navItems"
        :key="page"
        :href="`#${page}`"
        :class="{ 'bg-gray-200 pointer-events-none': page == currentPage }"
        v-on:click="currentPage = page"
      >
        <component :is="icon" class="TheNavListIcons" /> {{ page }}
      </NavItem>
    </ul>
  </nav>
</template>
