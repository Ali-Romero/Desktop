<template>
  <div class="sidebar-info">
    <div class="sidebar-info__title">
      OneDrive Storage:
    </div>
    <div class="sidebar-info__text">
      1.51 GB used of 5 GB
    </div>
    <div class="sidebar-info__progress">
      <div />
    </div>
  </div>
</template>

<style lang="sass" scoped>
.sidebar-info
  &__title
    font-size: 14px
    line-height: 20px
    font-weight: 600
    margin-bottom: 4px

  &__text
    font-size: 12px
    line-height: 16px
    margin-bottom: 8px

  &__progress
    height: 15px
    background-color: #fff
    border-radius: 2px
    overflow: hidden

    div
      height: 100%
      width: 45%
      background-color: #926ba2
</style>
