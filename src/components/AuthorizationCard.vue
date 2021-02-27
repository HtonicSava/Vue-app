<template>
  <div class="AuthorizationCard">
    <form class="AuthorizationCard__content">
      <h2 class="AuthorizationCard__title">Авторизация</h2>
      <h3 class="AuthorizationCard__subtitle">
        Если у вас уже существует аккаунт,
        вы можете войти в него
      </h3>
      <div class="AuthorizationCard__field">
        <div class="AuthorizationCard__inputLogin">
          <input type="text" class="AuthorizationCard__login" placeholder="Логин" />
          <div class="AuthorizationCard__loginimg AuthorizationCard__img"></div>
        </div>
        <div class="AuthorizationCard__inputPassword">
          <input type="text" class="AuthorizationCard__password" placeholder="Пароль" />
          <div class="AuthorizationCard__passwordimg AuthorizationCard__img"></div>
        </div>

        <div class="AuthorizationCard__subinput">
          <Checkbox class="AuthorizationCard__checkbox" msg="Запомнить" />
          <a href="#" class="AuthorizationCard__passMsg">Забыли пароль?</a>
        </div>
      </div>

      <Vbutton class="AuthorizationCard__button" msg="Войти" />
      <p class="AuthorizationCard__bottomText">
        Нет аккаунта?
        <a href="#" class="AuthorizationCard__bottomLink">Зарегистрироваться</a>
      </p>
    </form>
  </div>
</template>


<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";
import Vbutton from "./Vbutton.vue";
import Checkbox from "./Checkbox.vue";

@Component({
  components: {
    Vbutton,
    Checkbox
  }
})
export default class AuthorizationCard extends Vue {
  //   @Prop() private msg!: string;
}
</script>

<style scoped lang="scss">
.AuthorizationCard {
  width: 500px;
  height: 649px;
  background: #ffffff;
  border-radius: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.AuthorizationCard__content {
  width: 295px;
  text-align: center;
}

.AuthorizationCard__title {
  margin-bottom: 22px;
  font-family: inter;
  font-weight: 500;
  font-size: 24px;
  line-height: 29px;
  color: #000000;
}
.AuthorizationCard__subtitle {
  margin-bottom: 65px;
  color: #aaaaaa;
  font-size: 16px;
  line-height: 19px;
}

.AuthorizationCard__field {
  margin-bottom: 58px;
}

.AuthorizationCard__inputLogin,
.AuthorizationCard__inputPassword {
  position: relative;
}

.AuthorizationCard__login {
  margin-bottom: 28px;
}

.AuthorizationCard__password {
  margin-bottom: 35px;
}

.AuthorizationCard__login,
.AuthorizationCard__password {
  width: 295px;
  border-bottom: 2px solid #dedede;
  padding-bottom: 12px;
  padding-left: 29px;
  transition: 0.5s;
}

.AuthorizationCard__login::placeholder,
.AuthorizationCard__password::placeholder {
  color: #595959;
  font-weight: 500;
  font-size: 18px;
  line-height: 22px;
  transition: 0.5s;
}

.AuthorizationCard__login:focus,
.AuthorizationCard__password:focus {
  border-bottom: 2px solid #0755ff;
}

.AuthorizationCard__login:focus ~ .AuthorizationCard__loginimg {
  background-image: url("~@/assets/login-blue.png");
}

.AuthorizationCard__password:focus ~ .AuthorizationCard__passwordimg {
  background-image: url("~@/assets/password-blue.png");
}

.AuthorizationCard__login:focus::placeholder,
.AuthorizationCard__password:focus::placeholder {
  color: #0755ff;
}

.AuthorizationCard__img {
  height: 18px;
  width: 14px;
  position: absolute;
  left: 0;
  top: 0;
  transition: 0.5s;
}

.AuthorizationCard__loginimg {
  background-image: url("~@/assets/login.png");
}

.AuthorizationCard__passwordimg {
  background-image: url("~@/assets/password.png");
}

.AuthorizationCard__subinput {
  font-weight: 500;
  font-size: 16px;
  line-height: 19px;
  color: #aaaaaa;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.AuthorizationCard__label {
  margin-right: 49px;
}

.AuthorizationCard__passMsg {
  margin-bottom: 4px;
}

.AuthorizationCard__bottomText {
  margin-top: 30px;
  color: #aaaaaa;
}

.AuthorizationCard__bottomLink {
  color: #0075ff;
}
</style>