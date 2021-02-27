<template>
  <button>
    <!-- <p>Войти</p> -->
    <p>{{msg}}</p>
  </button>
</template>


<script lang="ts">
import { Component, Vue, Prop } from "vue-property-decorator";

@Component
export default class Vbutton extends Vue {
  @Prop() private msg!: string;
}
</script>

<style scoped lang="scss">
button {
  background: #0075ff;
  border-radius: 83px;
  // position: relative;
  width: 295px;
  height: 41px;
  transition: 0.5s;
}

button:hover {
  filter: drop-shadow(0px 9px 28px rgba(0, 0, 0, 0.2));
}

p {
  position: relative;
  font-weight: 500;
  font-size: 18px;
  line-height: 22px;
  margin: 0;
  color: #ffffff;
}
</style>