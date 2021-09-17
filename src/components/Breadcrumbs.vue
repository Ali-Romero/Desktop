<template>
  <div class="breadcrumbs">
    <div class="breadcrumbs__icon">
      <img src="@/assets/icons/folder.svg" class="d-block" alt="folder" width="16" height="16" />
    </div>

    <div class="breadcrumbs__text">
      <slot />
    </div>
  </div>
</template>

<style lang="sass" scoped>
.breadcrumbs
  flex: 1
  display: flex
  align-items: center
  padding: 8px
  background-color: #FFF
  border-radius: 2px
  font-size: 12px
  line-height: 16px

  &__icon
    margin-right: 12px

  &__text
    white-space: nowrap
    text-overflow: ellipsis
    overflow: hidden
</style>
