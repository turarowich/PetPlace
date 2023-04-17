<template>
    <div class="advertisement">
        РЕКЛАМА        
    </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'AdvertisementComp'
})
</script>

<style scoped lang="scss">
.advertisement{
    background: #D9D9D9;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 64px;
    color: #fff;
    height: 400px;
}
</style>