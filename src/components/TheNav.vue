<script setup>
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
</script>

<template>
  <nav class="TheNav">
    <ul class="TheNavList">
      <NavItem v-for="(icon, page) in navItems" :key="page" :href="`#${page}`">
        <component :is="icon" class="TheNavListIcons" /> {{ page }}
      </NavItem>
    </ul>
  </nav>
</template>
