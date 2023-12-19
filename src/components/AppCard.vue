<template>
    <div class="card">
        <img :src="card.card_images[0].image_url" alt="">
        <h1>{{ card.name }}</h1>
        <p>{{ card.archetype }}</p>
    </div>
</template>
<script>
export default {
    name: 'AppCard',
    props:{
        card: {
            type: Object,
            required: true
        }
    },
}
</script>
<style lang="scss" scoped>
@import '../styles/partials/mixins';

    .card{
        width: 100%;
        height: 500px;
        background-color: #D48F38;
        @include flex(column,space-between,center);
        gap: 1rem;
        padding-bottom: 1rem;
        margin-bottom: 1rem;
        
        img{
            width: 100%;
        }
        h1{
            color: whitesmoke;
            text-align: center;
            // padding: 1rem;
        }
        p{
            text-align: center;
            // padding: 1rem 0rem;
        }
    }
</style>