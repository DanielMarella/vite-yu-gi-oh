<template>
    <div class="container">
        <div class="row">
            <div class="col-12">
                <h2 class="mb-5">
                    In questa pagina ci sono {{ this.cardList.length }} carte!
                </h2>
            </div>
        </div>

        <div class="row">
            <SingleCard v-for="card in cardList"
            :cardImg="card.card_images[this.index].image_url"
            :cardName="card.name"
            :cardType="card.archetype"
            />
        </div>
    </div>
</template>

<script>
import SingleCard from './SingleCard.vue';



export default {
    name : 'CardList',
    data() {
        return {
            index : 0,
        }
    },

    props : {
        cardList : Array,  
    },

    components: {
    SingleCard,
},
}
</script>

<style lang="scss" scoped>
    h2{
        color: white;
    }
</style>