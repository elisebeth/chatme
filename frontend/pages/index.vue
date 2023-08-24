<template>
  <main class="introduction">
    <img src="@/assets/icons/logo.svg" alt="logo" class="introduction__logo">
    <h2 class="introduction__title">Openland</h2>
    <p class="introduction__text">Modern social network<br>built for you, not advertisers</p>
    <NuxtLink href="/registration/phone" class="introduction__button">Continue with phone</NuxtLink>
    <NuxtLink href="/registration/email" class="introduction__button introduction__button_gray">Continue with email</NuxtLink>
  </main>
</template>

<script lang="ts" setup>

</script>

<style lang="stylus" scoped>
.introduction
  width 100vw
  height 100vh
  background #fff
  padding 15.625rem 0
  display flex
  flex-direction column
  align-items center

  &__logo
    width 8rem
    height 8rem
  
  &__title
    color #171A1F
    font-size 1.5rem
    font-weight 700
    margin-top 1rem
    margin-bottom 0.5rem
    letter-spacing -0.015rem
  
  &__text
    width 20rem
    color #71747A
    font-size 0.9375rem
    letter-spacing -0.015rem
    text-align center
    margin-bottom 2rem
  
  &__button
    display flex
    align-items center
    justify-content center
    width 15rem
    height 2.5rem
    border-radius 0.5rem
    outline none
    border 0.125rem solid #248BF2
    background #248BF2
    color #fff
    cursor pointer
    font-size 0.9375rem
    font-weight 600
    line-height 1.5rem
    letter-spacing -0.015rem
    text-decoration none
    transition background .25s, color .25s

    &:hover
      background #fff
      color #248BF2

    &:first-of-type
      margin-bottom 1rem

    &_gray
      background #F2F3F5
      border-color #F2F3F5
      color #71747A

      &:hover
        background #71747A
        color #F2F3F5
</style>