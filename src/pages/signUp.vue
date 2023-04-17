<template>
    <div class="signup">
      <h2 class="signup-title">Регистрация в личный кабинет</h2>
      <q-form
        class="signup-form"
      > 
        <div class="input-block">
          <label for="">Страна<span>*</span></label>
          <input class="signup-input" placeholder="Логин/email" type="text">
        </div>
        <div class="input-block">
          <label for="">Регион</label>
          <input class="signup-input" placeholder="Логин/email" type="text">
        </div>
        <div class="input-block">
          <label for="">Имя<span>*</span></label>
          <input class="signup-input" placeholder="Логин/email" type="text">
        </div>
        <div class="input-block">
          <label for="">Фамилия</label>
          <input class="signup-input" placeholder="Логин/email" type="text">
        </div>
        <div class="input-block">
          <label for="">Телефон<span>*</span></label>
          <input class="signup-input" placeholder="Логин/email" type="text">
        </div>
        <div class="input-block">
          <label for="">Email<span>*</span></label>
          <input class="signup-input" placeholder="Логин/email" type="text">
        </div>
        <div class="input-block">
          <label for="">Пароль</label>
          <input class="signup-input" placeholder="Логин/email" type="text">
        </div>
        <div class="input-block">
          <label for="">Потверждение пароля</label>
          <input class="signup-input" placeholder="Логин/email" type="text">
        </div>
        <q-btn class="signup-btn">
          Зарегистрироватся в лк
        </q-btn>
        <div class="signup-signin">
            <q-item-section avatar top>
                <q-checkbox val="cyan-5" color="cyan-5" />
            </q-item-section>
            <q-item-section>
                <q-item-label caption>
                Нажимая на кнопку регистрации, вы даете согласие на обработку персональных данных и соглаетесь с политикой конфиденциальности
                </q-item-label>
            </q-item-section>
            <!-- <q-checkbox value="true" label="Нажимая на кнопку регистрации, вы даете согласие на обработку персональных данных и соглаетесь с политикой конфиденциальности"/> -->
        </div>
      </q-form>
    </div>
  </template>
  
  <script>
  import { defineComponent } from 'vue'
  
  export default defineComponent({
    name: 'signUp',

  })
  </script>

<style scoped lang="scss">
.signup{
  width: 100%;
  min-height: 84vh;
  background: url(../assets/signup.png) no-repeat;
  background-size: cover;
  background-position: center -130px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  &-title{
    font-weight: 400;
  }
  &-form{
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    grid-row-gap: 20px;
    grid-column-gap: 29px;
    width: 740px;
    @media (max-width: 815px) {
        grid-template-columns: 1fr;
        width: 90%;
    }
  }
  .input-block{
    display: flex;
    flex-direction: column;
    gap: 10px;
    label{
        span{
            color: red;
        }
    }
  }
  &-input{
    background: $white;
    border: 1px solid #D9D9D9;
    width: 100%;
    height: 50px;
    padding: 0 15px;
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
  &-signin{
    display: flex;
    margin-top: 27px;
    justify-content: center;
    color: #0C0C0C;
    div{
        color: #0C0C0C;
    }
  }
}
</style>
  