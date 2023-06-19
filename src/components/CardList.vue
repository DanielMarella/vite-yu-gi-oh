<template>
    <div class="container">
        <div class="row">
            <div class="col-12">
                <h2>
                    Card List
                </h2>
            </div>
        </div>
        <div class="row">
            <SingleCard/>
        </div>
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