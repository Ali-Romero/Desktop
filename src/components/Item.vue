<template>
  <div class="item" v-bind="$attrs">
    <div class="item__image">
      <img :src="require(`@/assets/images/${mode}.png`)" :alt="mode" width="75" height="75" />
    </div>
    <div class="item__name">
      {{ name }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'Item',
  props: {
    mode: {
      type: String
    },
    name: {
      type: String
    }
  }
}
</script>

<style lang="sass" scoped>
.item
  width: 75px
  margin-bottom: 24px
  margin-right: 24px
  cursor: pointer

  &__image
    img
      display: block

  &__name
    font-size: 12px
    line-height: 16px
    text-align: center
</style>
