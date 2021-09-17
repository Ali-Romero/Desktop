<template>
  <aside class="sidebar">
    <div class="sidebar__explorer">
      <Explorer />
    </div>
    <div class="sidebar__spacer" />

    <div class="sidebar__bottom">
      <SidebarInfo />
    </div>
  </aside>
</template>

<script>
import Explorer from '@/components/Explorer'
import SidebarInfo from '@/components/SidebarInfo'

export default {
  name: 'Sidebar',
  components: {
    Explorer,
    SidebarInfo,
  }
}
</script>

<style lang="sass" scoped>
.sidebar
  height: calc(100% - 36px) // - padding
  padding: 18px
  display: flex
  flex-direction: column
  overflow: auto

  &__spacer
    flex: 1

  &__title
    margin-bottom: 32px
</style>
