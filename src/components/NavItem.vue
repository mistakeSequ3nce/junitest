<script>
export default {
  inheritAttrs: false,
}
</script>

<template>
  <li>
    <a v-bind="$attrs" class="TheNavListObject">
      <slot></slot>
    </a>
  </li>
</template>
