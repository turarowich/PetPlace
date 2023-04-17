<template>
    <div class="signin">
      <h2 class="signin-title">Вход в личный кабинет</h2>
      <q-form
        class="signin-form"
      > 
        <div class="input-block">
          <label for="">Логин</label>
          <input class="signin-input" placeholder="Логин/email" type="text">
        </div>
        <div class="input-block">
          <label for="">Пароль</label>
          <div class="signin-input-password">
            <input class="signin-input" placeholder="*******" type="password">
            <span>Забыли пароль</span>
          </div>
        </div>
        <q-btn class="signin-btn">
          Войти в личный кабинет
        </q-btn>
        <div class="signin-registration">
          <q-btn class="signin-registration-btn">
            регистрация
          </q-btn>
        <div>если у вас еще нет <br> аккаунта</div>
        </div>
      </q-form>
    </div>
  </template>
  
  <script>
  import { defineComponent } from 'vue'
  
  export default defineComponent({
    name: 'SignIn'
  })
  </script>

<style scoped lang="scss">
.signin{
  width: 100%;
  height: 84vh;
  background: url(../assets/singin.png) no-repeat;
  background-size: cover;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  @media (max-width: 815px) {
    background: #FAFAFA;
  }
  &-title{
    font-weight: 400;
  }
  &-form{
    display: flex;
    flex-direction: column;
    gap: 11px;
    width: 365px;
  }
  .input-block{
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
  &-input{
    background: $white;
    border: 1px solid #D9D9D9;
    width: 100%;
    height: 50px;
    padding: 0 15px;
  }
  &-input-password{
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: $white;
    border: 1px solid #D9D9D9;
    padding: 0 15px;
    input{
      border: none;
      outline: none;
      padding: 0;
    }
    span {
      color: rgb(48, 132, 214);
      white-space: nowrap;
      cursor: pointer;
    }
  }
  &-btn{
    text-transform: uppercase;
    width: 100%;
    font-size: 22px;
    font-weight: 600;
    background: $dark-blue;
    color: $white;
    margin-top: 30px;
  }
  &-registration{
    display: flex;
    gap: 10px;
    margin-top: 27px;
    &-btn{
      text-transform: uppercase;
      background: $dark-blue;
      color: $white;
      height: 34px;
    }
    div{
      line-height: 18px;
    }
  }
}
</style>
  