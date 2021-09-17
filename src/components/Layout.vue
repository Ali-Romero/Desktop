<template>
  <div class="layout">
    <div class="layout__window">
      <div class="layout__sidebar">
        <div class="layout__sidebar-inner">
          <slot name="sidebar" />
        </div>
      </div>
      <div class="layout__inner">
        <header class="layout__header">
          <slot name="button" />

          <slot name="breadcrumbs" />
        </header>
        <main class="layout__body">
          <slot name="main" />
        </main>
      </div>
    </div>
  </div>
</template>

<style lang="sass" scoped>
.layout
  padding: 0 15px
  display: flex
  align-items: center
  justify-content: center
  height: 100%
  background: url('~@/assets/images/bg.jpg') no-repeat
  background-size: cover

  &__window
    display: flex
    width: 100%
    max-width: 800px
    height: calc(100% - 80px)
    min-height: 300px
    max-height: 500px
    border-radius: 6px
    overflow: hidden
    box-shadow: 0 2px 5px #ccc

  &__sidebar
    display: none
    width: 180px
    position: relative

    &::after
      content: ""
      width: 100%
      height: 100%
      position: absolute
      top: 0
      left: 0
      background-color: #FFF
      opacity: 0.4
      z-index: 1

  &__sidebar-inner
    position: relative
    z-index: 5
    height: 100%

  &__inner
    background-color: #FFF
    flex: 1
    min-width: 1px

  &__header
    display: flex
    background-color: #f7f7f7
    padding: 18px

  &__body
    display: flex
    flex-wrap: wrap
    padding: 18px
    overflow: auto
    max-height: calc(100% - 104px) // header height + paddings

@media (min-width: 600px)
  .layout
    &__sidebar
      display: block
</style>
