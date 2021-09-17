<template>
  <div class="explorer">
    <div class="explorer__title">Explorer</div>

    <ExplorerItem>
      <template #icon>
        <img src="@/assets/icons/desktop.svg" class="d-block" alt="star" width="18" height="18" />
      </template>
      <template #text>
        Desktop
      </template>
    </ExplorerItem>

    <ExplorerItem>
      <template #icon>
        <img src="@/assets/icons/star.svg" class="d-block" alt="star" width="18" height="18" />
      </template>
      <template #text>
        Favorites
      </template>
    </ExplorerItem>

    <ExplorerItem>
      <template #icon>
        <img src="@/assets/icons/images.svg" class="d-block" alt="star" width="18" height="18" />
      </template>
      <template #text>
        Images
      </template>
    </ExplorerItem>
  </div>
</template>

<script>
import ExplorerItem from '@/components/ExplorerItem'

export default {
  name: 'Explorer',
  components: {
    ExplorerItem
  }
}
</script>

<style lang="sass" scoped>
.explorer
  &__title
    margin-bottom: 32px
</style>
