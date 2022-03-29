<template>
  <div class="p-20">
    <button class="btn btn-primary" @click="show = !show">Display</button>
    <Transition @enter="onEnter" appear name="fade">
      <h1 v-if="show">Bonjour !</h1>
    </Transition>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

function onEnter() {
  console.log('test');
}

const show = ref(true);
</script>

<style lang="scss">
@import './assets/scss/base.scss';

// .fade-enter-from,
// .fade-leave-to {
//   opacity: 0;
// }

// .fade-enter-to,
// .fade-leave-from {
//   opacity: 1;
// }

// .fade-leave-active,
.fade-enter-active {
  // transition: all 2s;
  animation: smallToBig 1s;
}

@keyframes smallToBig {
  0% {
    opacity: 0;
    font-size: 5px;
  }

  100% {
    opacity: 1;
    font-size: 32px;
  }
}
</style>
