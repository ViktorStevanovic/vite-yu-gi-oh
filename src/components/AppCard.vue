<template>
    <div>
        <h1>{{ card.name }}</h1>
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
    
</style>