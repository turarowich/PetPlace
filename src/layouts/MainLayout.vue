<template>
  <q-layout view="lHh Lpr lff">
    <q-header class="header">
      <div class="header-info">
        <div class="header-logo">
          <q-img class="header-logo-img" src="../assets/logo.png">
          </q-img>
          <h6 class="header-logo-text">Опыт, создающий дружбу навсегда</h6>
        </div>
        <div class="header-auth">
          <q-btn @click="$router.push('/signin')" class="header-auth-btn" label="Вход/регистрация" />
        </div>
      </div>
      <nav class="header-nav">
        <router-link v-for="(i,k) in headerMenu" :key="k" class="header-nav-link" :style="{backgroundColor: i.showing && '#4DAD98'}" :to="'/'">
          {{ i.name }}
          <q-menu v-model="i.showing" class="no-border no-border-radius" :style="{ backgroundColor: '#4DAD98', color: '#fff', boxShadow: 'none', borderRadius: 'none'}">
            <q-list style="min-width: 200px">
              <q-item v-for="(j,k) in i?.children || []" :key="k" clickable v-close-popup>
                <q-item-section>{{ j.name }}</q-item-section>
              </q-item>
            </q-list>
          </q-menu>
        </router-link>
      </nav>
    </q-header> 

    <q-page-container class="container">
      <router-view />
    </q-page-container>

    <q-footer class="footer">
      <div class="footer-contact">
        <div class="footer-contact-item">
          <h2 class="footer-contact-item-title text-uppercase">Телефон</h2>
          <h2 class="footer-contact-item-desc">+1 123 456 78 90</h2>
        </div>
        <div class="footer-contact-item">
          <h2 class="footer-contact-item-title text-uppercase">Почта</h2>
          <h2 class="footer-contact-item-desc">example@site.com</h2>
        </div>
        <div class="footer-contact-item">
          <h2 class="footer-contact-item-title">Социальные сети</h2>
          <h2 class="footer-contact-item-desc">+1 123 456 78 90</h2>
        </div>
      </div>
      <div class="footer-info">
        <nav class="footer-info-nav">
          <router-link class="footer-info-nav-link" to="/">Объявления</router-link>
          <router-link class="footer-info-nav-link" to="/">Услуги</router-link>
          <router-link class="footer-info-nav-link" to="/">Товары</router-link>
          <router-link class="footer-info-nav-link" to="/">Блог</router-link>
        </nav>
        <div class="footer-info-text">
          © All Rights Reserved. Acme Design Co. <br>
          <span>hello@mysite.com</span>
        </div>
      </div>
    </q-footer>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'MainLayout',

  components: {
  },

  setup () {
    const leftDrawerOpen = ref(false)
    const headerMenu = ref([
      {
        name: 'Объявления',
        children: [
          {
            name: 'Подбор породы'
          },
          {
            name: 'Купить собаку'
          }
        ],
        showing: false
      },
      {
        name: 'Услуги',
        showing: false
      },
      {
        name: 'Товары',
        showing: false
      },
      {
        name: 'Блог',
        showing: false
      }
    ])
    return {
      headerMenu,
    }
  }
})
</script>

<style scoped lang="scss">
.footer{
  background: $white;
  &-info{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    width: 100%;
    background: $dark-blue;
    border-radius: 50px 50px 0px 0px;
    height: 300px;
    gap: 61px;
    &-text{
      text-align: center;
      font-style: 15px;
      color: $white;
    }
    &-nav{
      display: flex;
      justify-content: center;
      align-items: center;
      &-link{
        text-decoration: none;
        color: $white;
        width: 200px;
        border-right: 1px solid $white;
        display: flex;
        align-items: center;
        justify-content: center;
        &:last-child{
          border-right:none;
        }
      }
    }
  }
  &-contact{
    display: flex;
    align-items: center;
    justify-content: center;
    background: $silver;
    border-radius: 50px 50px 0px 0px;
    width: 100%;
    height: 211px;
    &-item{
      padding: 0 4%;
      color: $dark;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      &-title{
        font-size: 24px;
        font-weight: 600;
      }
      &-desc{
        font-size: 24px;
        font-weight: 600;
      }
      &:nth-child(2){
        border-right: 1px solid $black;
        border-left: 1px solid $black;
      }
    }
  }
  @media (max-width: 815px) {
    border-radius: none;
    &-info-nav{
      display: none;
    } 
    &-info{
      border-radius: 0;
      height: 80px;
      gap: 0;
    }
    &-contact{
      border-radius: 0;
      flex-direction: column;
      background: $dark-blue;
      &-item:nth-child(2){
        border: none;
      }
      &-item{
        color: $white;
      }
      &-item-title{
        display: none;
      }
    }
  }
}
.header{
  background: #fff;
  &-nav{
    display: flex;
    width: 100%;
    background: $dark-blue;
    justify-content: center;
    align-items: center;
    height: 50px;
    &-link{
      height: 45px;
      text-decoration: none;
      color: $white;
      width: 200px;
      border-left: 1px solid $white;
      display: flex;
      align-items: center;
      justify-content: center;
      &:last-child{
        border-right: 1px solid $white;
      }
    }
  }
  &-info{
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    padding: 20px 4%;
    max-width: 1320px;
    margin: 0 auto;
  }
  &-logo{
    display: flex;
    align-items: center;
    width: 40%;
    height: 82px;
    &-img{
      padding: 0;
      max-height: 96px;
      img{
        object-fit: cover !important;
      }
    }
    &-text{
      color: $dark;
    }
  }
  &-auth{
    &-btn{
      background: $orange;
      text-transform: none;

    }
  }

}
</style>