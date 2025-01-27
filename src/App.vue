<script setup>
import {
  HomeIcon,
  IdentificationIcon,
  ListBulletIcon,
  ChatBubbleLeftIcon,
} from '@heroicons/vue/24/outline'

const mainPage = 'Главная страница'
const postsListPage = 'Список постов'
const usersListPage = 'Список пользователей'
const commentsPage = 'Комментарии'
const navItems = [mainPage, postsListPage, usersListPage, commentsPage]
</script>

<template>
  <header class="TheHeader">
    <a href="#">
      <img
        src="./assets/1724866703chatgpt-logo-with-no-background.png"
        alt="logo"
        class="TheLogo"
      />
    </a>
  </header>
  <main class="PageMain"></main>
  <nav class="TheNav">
    <ul class="TheNavList">
      <li v-for="page in navItems" :key="page">
        <a :href="`#${page}`" class="TheNavListObject">
          <HomeIcon v-if="page == mainPage" class="TheNavListIcons" />
          <ListBulletIcon v-else-if="page == postsListPage" class="TheNavListIcons" />
          <IdentificationIcon v-else-if="page == usersListPage" class="TheNavListIcons" />
          <ChatBubbleLeftIcon v-else class="TheNavListIcons" /> {{ page }}
        </a>
      </li>
    </ul>
  </nav>
</template>
