<template>
    <div>
        <article v-for="card in store.cardsList" :key="card.id" >
            <AppCard :card="card"/>

        </article>
    </div>
</template>
<script>
import AppCard from './AppCard.vue';
import { store } from '../js/store.js';


export default {
    name: 'AppCardslist',
    components:{
        AppCard
    },
    data() {
        return {
            store
        }
    },
}
</script>
<style lang="scss" scoped>
    
</style>