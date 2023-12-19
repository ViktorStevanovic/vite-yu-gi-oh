<template>
    
    <section class="card-container">
        <article v-for="card in store.cardsList" :key="card.id" >
            <AppCard :card="card"/>
        </article>
    </section>
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
@import '../styles/partials/mixins';

    .card-container{
        background-color: white;
        width: 90%;
        padding: 2rem;
        @include flex(row,space-between,center);
        flex-wrap: wrap;
        gap: 1rem;
    }
    article{     
       width: calc(100% / 6);
       height: 350px;
    }
</style>