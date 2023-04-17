<template>
    <div class="card">
        <q-img class="card-img" src="../../assets/options1.png"></q-img>
        <div class="card-content">
            <div class="card-title">Название товара</div>
            <div class="card-option">Вес упаковки</div>
            <div class="card-option">Назначение корма, какое-то описание</div>
            <div class="card-price">
            <span> Цена: </span>  <strong>5 000 ₽</strong>
            </div>
            <div class="card-buttons">
                <q-btn style="background: #F1942C; color: white" label="В корзину"></q-btn>
                <q-icon  size="1.2em" name="favorite_border"></q-icon>
            </div>
        </div>
    </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'CardProduct'
})
</script>

<style scoped lang="scss">
.card{
    border: 1px solid silver;
    width: 100%;
    border-radius: 5px;
    &-img{
        height: 200px;
    }
    &-info{
      font-weight: 600;
      color: $white;
    }
    &-content{
        padding: 8px 11px;
    }
    &-title{
        font-weight: 600;
        font-size: 16px;
        line-height: 19px;
        color: $dark;
    }
    &-option{
        font-weight: 300;
        font-size: 12px;
        line-height: 14px;
        color: $dark;
    }
    &-price{
        margin: 12px 0;
        span{
            font-weight: 300;
            font-size: 12px;
            line-height: 14px;
            color: $dark;
        }
        strong{
            font-weight: 600;
            font-size: 16px;
            line-height: 19px;
            color: $dark;
        }
    }
    &-buttons{
        display: flex;
        align-items: center;
        justify-content: space-between;
        button{
            color: $white;
            background: $orange;
        }
    }
}
</style>