<template>
  <div class="sandbox">
    <button class="sandbox__button" @click="show = !show">{{ show ? 'Hide' : 'Show' }}</button>
    <transition name="rolling" enter-active-class="animated rollIn" leave-active-class="animated rollOut">
      <img class="sandbox__image animated" v-show="show" src="../assets/images/vuejs_logo.png" alt="vuejs">
    </transition>
  </div>
</template>

<script>
  import '../assets/stylesheet/index.css'
  import 'animate.css'

  export default {
    name: 'Sandbox',
    data () {
      return {
        show: false
      }
    }
  }
</script>
