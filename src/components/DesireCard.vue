<template>
  <div class="card">
    <div class="card__text">
      <h1 class="card__title">Desire RolePlay</h1>
      <h3 class="card__subtitle">Лучший проект игровых серверов за всю историю GTA V</h3>
    </div>
  </div>
</template>


<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class DesireCard extends Vue {
  //   @Prop() private msg!: string;
}
</script>

<style scoped lang="scss">
.card {
  width: 489px;
  height: 649px;
  position: relative;
  background-image: url("~@/assets/cardimage.png");

  border-radius: 20px 0px 0px 20px;
}
.card::before {
  content: "";
  background: rgba(0, 119, 255, 0.85);
  width: 489px;
  height: 649px;
  position: absolute;
  border-radius: 20px 0px 0px 20px;
}

.card__text {
  width: 269px;
  height: 184px;
  position: relative;
  top: 208px;
  left: 92px;
}

.card__title {
  font-weight: bold;
  font-size: 54px;
  line-height: 65px;

  color: #ffffff;
  margin-bottom: 16px;
}

.card__subtitle {
  font-weight: 500;
  font-size: 16px;
  line-height: 19px;

  color: #ffffff;
}
</style>