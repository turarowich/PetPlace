<template>
    <div class="card">
        <q-img class="card-img" src="../../assets/options1.png">
            <h2 class="card-info absolute-full flex flex-center">Собаки</h2>
        </q-img>
    </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'CardBase'
})
</script>

<style scoped lang="scss">
.card{
    width: 100%;
    &-img{
        height: 320px;
    }
    &-info{
      font-weight: 600;
      color: $white;
    }
}
</style>