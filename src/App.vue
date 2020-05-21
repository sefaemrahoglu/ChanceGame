<template>
  <transition-group name="slideContainer" mode="out-in">
    <component key="mainComponent" @activeComponentEvent="activeComponent = $event" :is="activeComponent"></component>
    <canvas key="canvas" id="canvas" v-show="activeComponent == 'app-Celebrate'"></canvas>
  </transition-group>
</template>

<script>
import Celebrate from "./components/Celebrate";
import Failure from "./components/Failure";
import GameCards from "./components/GameCards";
export default {
  components: {
    appGameCards: GameCards,
    appCelebrate: Celebrate,
    appFailure: Failure
  },
  data() {
    return {
      activeComponent: "app-Game-Cards"
    };
  }
};
</script>

<style>
body {
  font-family: sans-serif;
  background: #dddddd;
}
.slideContainer-enter {
}
.slideContainer-enter-active {
  animation: slide-in 0.3s ease-out forwards;
}
.slideContainer-leave {
}
.slideContainer-leave-active {
  animation: slide-out 0.3s ease-out forwards;
}
@keyframes slide-in {
  from {
    transform: translateX(-1000px);
    opacity: 0;
  }
  to {
    transform: translateX(0px);
    opacity: 1;
  }
}
@keyframes slide-out {
  from {
    transform: translateX(0px);
    opacity: 1;
  }
  to {
    transform: translateX(1000px);
    opacity: 0;
  }
}
</style>