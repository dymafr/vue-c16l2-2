<template>
  <div class="p-20">
    <button class="btn btn-primary" @click="show = !show">Cliquez !</button>
    <Transition @enter="onEnter" appear name="fade">
      <p v-if="show">
        Principes fertur et exitiale aliquando oblato factitarunt quod
        propositum quod illo ob illo numquam obstinatum obstinatum quoque
        aetatis revocari iussisse vitium factitarunt inexorabiles aetatis quod
        accendente fertur aetatis iussisse vitium similia iussisse factitarunt
        propositum similia neminem revocari adulatorum accendente fertur ob
        adulatorum principes accendente inexorabiles elogio vitium exitiale
        aliis progressu eius eius eius et non quoque vel in in quod more de
        propositum quod oblato factitarunt poenae hoc principes exitiale cohorte
        hoc similia hoc aliis quod de in in addictum eius adulatorum quoque et
        ob oblato neminem numquam adulatorum addictum ob quod cohorte aliis
        neminem vel revocari hoc hoc similia.
      </p>
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
