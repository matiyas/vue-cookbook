<template>
  <div class="sandbox">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.7.2/animate.min.css">
    <button class="sandbox__button" @click="show = !show">{{ show ? 'Hide' : 'Show' }}</button>
    <transition name="rolling" enter-active-class="animated rollIn" leave-active-class="animated rollOut">
      <img class="sandbox__image animated" v-show="show" src="./images/vuejs_logo.png" alt="vuejs">
    </transition>
  </div>
</template>

<script>
  import './stylesheet/index.css'

  export default {
    name: 'Sandbox',
    data () {
      return {
        show: false
      }
    }
  }
</script>
