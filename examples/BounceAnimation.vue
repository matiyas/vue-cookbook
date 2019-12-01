<template>
  <div class="sandbox">
    <button class="sandbox__button" @click="show = !show">Show</button>
    <transition name="bounce">
      <img class="sandbox__image" v-show="show" src="../assets/images/vuejs_logo.png" alt="vuejs">
    </transition>
  </div>
</template>

<script>
  import '../assets/stylesheet/index.css'

  export default {
    name: 'BounceAnimation',
    data () {
      return {
        show: false
      }
    }
  }
</script>

<style scoped>
  @keyframes bounce {
    0% {
      transform: scale(0);
    }
    50% {
      transform: scale(1.5);
    }
    100% {
      transform: scale(1)
    }
  }

  .bounce-enter-active {
    animation: bounce .5s;
  }
  .bounce-leave-active {
    animation: bounce .5s reverse;
  }
</style>