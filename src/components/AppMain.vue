<template>
    <section>
        <h1>Main</h1>
        <AppCardslist :cardsList="cards"/>
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
            cards:[],
            store,
        }
    },
    methods: {
    getCards(){
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
      .then((response) => {
        // handle success
        console.log(response.data.data);
        this.store.cardsList = response.data.data;
      })
      .catch(function (error) {
        // handle error
        console.error(error);
      });
    }
  },
  created() {
    this.getCards()
  },
}
</script>
<style lang="scss" scoped>
    section{
        background-color: #D48F38;
        height: 800px;
    }
</style>