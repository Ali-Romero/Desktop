<template>
  <div class="item-icon">
    <div class="item-icon__icon">
      <slot name="icon" />
    </div>

    <slot name="text" />
  </div>
</template>

<style lang="sass" scoped>
.item-icon
  display: flex
  align-items: center
  font-size: 14px
  line-height: 16px
  color: #333
  margin-bottom: 10px

  &__icon
    margin-right: 12px
</style>
