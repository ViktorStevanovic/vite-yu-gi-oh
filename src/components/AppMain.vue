<template>
    <section>
        <h1>Main</h1>
        <AppCardslist/>
    </section>
</template>
<script>
import AppCardslist from './AppCardslist.vue';
import { store } from '../js/store.js';
import axios from 'axios';

export default {
    name:'AppMain',
    components:{
        AppCardslist,
    
    },
    data() {
        return {
            store,
        }
    },
}
</script>
<style lang="scss" scoped>
    section{
        background-color: #D48F38;
        height: 800px;
    }
</style>