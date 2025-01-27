<script setup>
import {
  HomeIcon,
  IdentificationIcon,
  ListBulletIcon,
  ChatBubbleLeftIcon,
} from '@heroicons/vue/24/outline'
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
      <li>
        <a href="#main_page" class="TheNavListObject">
          <HomeIcon class="TheNavListIcons" /> Главная страница
        </a>
      </li>
      <li>
        <a href="#posts_list_page" class="TheNavListObject">
          <ListBulletIcon class="TheNavListIcons" /> Список постов</a
        >
      </li>
      <li>
        <a href="#users_list_page" class="TheNavListObject">
          <IdentificationIcon class="TheNavListIcons" /> Список пользователей</a
        >
      </li>
      <li>
        <a href="#comments_page" class="TheNavListObject">
          <ChatBubbleLeftIcon class="TheNavListIcons" /> Комментарии</a
        >
      </li>
    </ul>
  </nav>
</template>
