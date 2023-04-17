<template>
  <q-page class="main">
      <div class="welcome">
        <h1 class="welcome-title">Заголовок / Уникальное торговое предложение</h1>
        <h2 class="welcome-sub-title">Заголовок </h2>
        <div class="welcome-search">
          <q-input class="welcome-search-input" square standout label="Поиск" > 
            <template v-slot:append>
              <router-link class="welcome-search-settings" to="/">Расширенный поиск</router-link>
            </template>
          </q-input>
          <q-btn icon="search"></q-btn>
        </div>
      </div>
      <div class="options">
        <h2 class="options-title">Выберите своего нового друга</h2>
        <div class="options-list">
          <CardBase />
          <CardBase />
        </div>
        <div class="options-list">
          <CardBase />
          <CardBase />
          <CardBase />
        </div>
        <div class="options-list">
          <CardBase />
          <CardBase />
        </div>
      </div>
      <div class="anouncements">
        <h2 class="anouncements-title">
          ТОП-объявления
        </h2>
        <div class="anouncements-list" style="gap: 20px">
          <div class="anouncements-item">
            <q-img class="anouncements-item-img" src="../assets/options1.png">
              <h3 class="anouncements-item-title absolute-top card-title">Кошки</h3>
              <div class="anouncements-item-info absolute-bottom-left">
                  <div >Вид</div>
                  <div>Порода</div>
                  <div class="card-title">ХХХ руб</div>
              </div>
            </q-img>
          </div>
          <div class="anouncements-item">
            <q-img class="anouncements-item-img" src="../assets/options1.png">
              <h3 class="anouncements-item-title absolute-top card-title">Кошки</h3>
              <div class="anouncements-item-info absolute-bottom-left">
                  <div >Вид</div>
                  <div>Порода</div>
                  <div class="card-title">ХХХ руб</div>
              </div>
            </q-img>
          </div>
          <div class="anouncements-item">
            <q-img class="anouncements-item-img" src="../assets/options1.png">
              <h3 class="anouncements-item-title absolute-top card-title">Кошки</h3>
              <div class="anouncements-item-info absolute-bottom-left">
                  <div >Вид</div>
                  <div>Порода</div>
                  <div class="card-title">ХХХ руб</div>
              </div>
            </q-img>
          </div>
          <div class="anouncements-item">
            <q-img class="anouncements-item-img" src="../assets/options1.png">
              <h3 class="anouncements-item-title absolute-top card-title">Кошки</h3>
              <div class="anouncements-item-info absolute-bottom-left">
                  <div >Вид</div>
                  <div>Порода</div>
                  <div class="card-title">ХХХ руб</div>
              </div>
            </q-img>
          </div>
        </div>
      </div>
      <Advertisement />
      <div class="pp-tell">
        <h2 class="pp-tell-title">Pets.Place расскажет для вас</h2>
        <div class="pp-tell-list">
          <CardBase />
          <CardBase />
          <CardBase />
        </div>
        <div class="pp-tell-list">
          <CardBase />
          <CardBase />
        </div>
        <div class="pp-tell-list">
          <CardBase />
          <CardBase />
          <CardBase />
        </div>
      </div>
      <div class="buy">
        <h2 class="buy-title">У нас вы можете купить</h2>
        <div class="buy-list">
          <CardBase />
          <CardBase />
          <CardBase />
        </div>
        <div class="buy-list">
          <CardBase />
          <CardBase />
        </div>
        <div class="buy-list">
          <CardBase />
          <CardBase />
          <CardBase />
        </div>
      </div>
      <div class="products">
        <div class="products-title-block">
          <h2 class="products-title">Популярные товары</h2>
          <q-btn class="products-title-btn" icon-right="trending_flat" label="Смотреть все">
          </q-btn>
        </div>
        <div class="products-list">
          <CardProduct />
          <CardProduct />
          <CardProduct />
          <CardProduct />
          <CardProduct />
          <CardProduct />
        </div>
      </div>
      <Advertisement />
      <div class="services">
        <h2 class="services-title">Наши услуги</h2>
        <div class="services-list">
          <CardBase />
          <CardBase />
          <CardBase />
          <CardBase />
        </div>
        <div class="services-list">
          <CardBase />
          <CardBase />
          <CardBase />
          <CardBase />
        </div>
        <div class="services-list">
          <CardBase />
          <CardBase />
          <CardBase />
          <CardBase />
        </div>
      </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'
import Advertisement from '../components/base/advertisement.vue'
import CardBase from '../components/base/card.vue'
import CardProduct from '../components/base/card-product.vue'


export default defineComponent({
  name: 'IndexPage',
  components: {
    Advertisement,
    CardBase,
    CardProduct
  }
})
</script>


<style scoped lang="scss">
.main{

}
.products{
  margin: 60px auto;
  padding: 60px 4%;
  max-width: 1320px;
  &-title-block{
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 60px;
  }
  &-title-btn{
    height: 50px;
    background: $orange;
    color: $white;
  }
  &-title{
    color: $dark;
    text-transform: uppercase;
  }
  &-list{
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
    width: 100%;
    margin: 20px 0;
  } 
  @media (max-width: 815px) {
    padding: 0;
    &-title{
      width: 100%;
      margin-top: 20px;
      padding: 0 4%;
      text-align: center;
      height: 50px;
      background: $dark-blue;
      color: $white;
      margin-bottom: 0;
    }
    &-title-btn{
      display: none;
    }
    &-list{
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-gap: 10px;
      padding: 0 4%;
      margin: 0;
    }
  }
}
.buy{
  margin: 60px auto;
  background: rgba(34, 160, 148, 0.3);
  padding: 60px 4%;
  border-radius: 50px;
  max-width: 1320px;
  &-title{
    color: $dark;
    text-align: center;
    margin-bottom: 60px;
    text-transform: uppercase;
  }
  &-list{
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
    width: 100%;
    margin: 20px 0;
  } 
  @media (max-width: 815px) {
    padding: 0;
    &-title{
      margin-top: 20px;
      padding: 0 4%;
      text-align: center;
      height: 50px;
      background: $dark-blue;
      color: $white;
      margin-bottom: 0;
    }
    &-list{
      flex-wrap: wrap;
      gap: 0;
      margin: 0;
    }
  }
}
.services{
  margin: 60px auto;
  background: $light-orange;
  padding: 60px 4%;
  border-radius: 50px;
  max-width: 1320px;
  &-title{
    color: $dark;
    text-align: center;
    margin-bottom: 60px;
    text-transform: uppercase;
  }
  &-list{
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
    width: 100%;
    margin: 20px 0;
  } 
  @media (max-width: 815px) {
    padding: 0;
    &-title{
      margin-top: 20px;
      padding: 0 4%;
      text-align: center;
      height: 50px;
      background: $dark-blue;
      color: $white;
      margin-bottom: 0;
    }
    &-list{
      flex-wrap: wrap;
      gap: 0;
      margin: 0;
    }
  }
}
.pp-tell{
  margin: 60px auto;
  background: $light-orange;
  padding: 60px 4%;
  border-radius: 50px;
  max-width: 1320px;
  &-title{
    color: $dark;
    text-align: center;
    margin-bottom: 60px;
    text-transform: uppercase;
  }
  &-list{
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
    width: 100%;
    margin: 20px 0;
  } 
  @media (max-width: 815px) {
    padding: 0;
    &-title{
      margin-top: 20px;
      padding: 0 4%;
      text-align: center;
      height: 50px;
      background: $dark-blue;
      color: $white;
      margin-bottom: 0;
    }
    &-list{
      flex-wrap: wrap;
      gap: 0;
      margin: 0;
    }
  }
}
.anouncements{
  padding: 60px 4%;
  max-width: 1320px;
  margin: 0 auto;
  &-title{
    color: $dark;
    margin-bottom: 60px;
  }
  &-list{
    display: flex;
    gap: 20px;
  }
  &-item{
    width: 100%;
    &-img{
      height: 400px;
    }
    &-title{
      color: $white;
      font-weight: 600;
      font-size: 24px;
      line-height: 28px;
      text-transform: uppercase;
      padding: 20px;
    }
    &-info{
      display: flex;
      flex-direction: column;
      background: transparent;
    }
  }
  @media (max-width: 815px) {
    padding: 0;
    &-title{
      margin-top: 20px;
      padding: 0 4%;
      text-align: center;
      height: 50px;
      background: $dark-blue;
      color: $white;
    }
    &-list{
      flex-wrap: wrap;
      padding: 0 4%;
      gap: 5px;
      margin: 5px 0;
    }
  }

}
.options{
  background: $light-blue;
  padding: 60px 4%;
  border-radius: 0 0 50px 50px;
  max-width: 1320px;
  margin: 0 auto;
  &-title{
    color: $dark;
    text-align: center;
    margin-bottom: 60px;
  }
  &-list{
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
    width: 100%;
    margin: 20px 0;
  }
  @media (max-width: 815px) {
    padding: 0;
    &-title{
      height: 50px;
      background: $dark-blue;
      color: $white;
    }
    &-list{
      flex-wrap: wrap;
      padding: 0 4%;
      gap: 5px;
      margin: 5px 0;
    }
  }
}
.welcome{
  width: 100%;
  height: calc(100vh - 186px);
  background: linear-gradient(0deg, rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.2)), linear-gradient(0deg, rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.2)), url(../assets/welcome.png);
  background-repeat: no-repeat;
  background-size: cover;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  gap: 28px;
  padding: 0px 4%;
  &-title {
    color: $white;
    text-align: center;
    text-transform: uppercase;
  }
  &-sub-title{
    color: $white;
    text-align: center;
  }
  &-search{
    display: flex;
    width: 70%;
    margin-top: 82px;
    &-settings{
      font-size: 18px;
      line-height: 21px;
      text-align: right;
      text-decoration-line: underline;
      color: $lightdark;
    }
    &-input{
      width: 100%;
      background: $white;
    }
    button{
      background: #F1942C;
      color: $white;
      border-radius: none;
    }
  }
  @media (max-width: 815px) {
    background-position: center;
    &-sub-title{
      display: none;
    }
    &-search{
      width: 90%;
      &-settings{
        display: none;
      }
    }
  }
}
</style>