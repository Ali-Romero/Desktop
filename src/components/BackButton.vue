<template>
  <button v-bind="$attrs" class="back-button" aria-label="back button">
    <img src="@/assets/icons/back.svg" class="d-block" alt="arrow" width="18" height="18" />
  </button>
</template>

<style lang="sass" scoped>
.back-button
  padding: 0 12px 0 0
  background: none
  border: none
  outline: none
  cursor: pointer

  &:disabled
    cursor: not-allowed
    opacity: 0.6
</style>
