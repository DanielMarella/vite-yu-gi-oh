<template>
    <div>
        <h2>
            Card List
        </h2>
        <SingleCard/>
    </div>
</template>

<script>
import SingleCard from './SingleCard.vue';

export default {
    name : 'CardList',
    data() {
        return {
            
        }
    },

    components: {
        SingleCard
    }
}
</script>
<style lang="scss" scoped>
    
</style>