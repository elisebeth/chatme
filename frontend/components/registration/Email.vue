<template>
  <form @submit.prevent="submit" class="registration">
    <h2 class="registration__title">What’s your email?</h2>
    <p class="registration__text">We’ll send you a sign-in code</p>
    <input v-model.trim="email" type="email" class="registration__input" placeholder="Email">
    <button class="registration__button">Next</button>
  </form>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const email = ref<string | null>(null);
const router = useRouter()

const submit = () => {
  if (!email.value) {
    alert('ti pidor vvedi email suko!')
  } else {
    router.push('/registration/code')
  }
}
</script>

<style lang="stylus" scoped>
.registration
  width 100vw
  height 100vh
  display flex
  flex-direction column
  align-items center
  justify-content center

  &__title
    color #171A1F
    font-size 1.5rem
    font-weight 700
    letter-spacing 0.0225rem
  
  &__text
    color #71747A
    font-size 0.9375rem
    line-height 1.5rem
    letter-spacing -0.015rem
    margin-bottom 2rem
  
  &__input
    width 20rem
    outline none
    padding 0.5rem 1rem
    background rgba(201, 204, 209, 0.24)
    color #171A1F
    border none
    font-size 0.9375rem
    line-height 1.5rem
    letter-spacing -0.015rem
    margin-bottom 2rem
  
  &__button
    background #248BF2
    color #FFFFFF
    border-radius 0.5rem
    font-size 0.9375rem
    font-weight 600
    letter-spacing -0.015rem
    line-height 1.5rem
    text-decoration none
    padding 0.375rem 1.5rem
    border 0.125rem solid #248BF2
    cursor pointer
    transition background .25s, color .25s

    &:hover
      background #fff
      color #248BF2
</style>