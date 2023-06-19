<template>
    <div class="container">
        <div class="row">
            <div class="col-12">
                <h2>
                    Card List :
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
import axios from 'axios';
export default {
    name : 'CardList',
    data() {
        return {
            cardList : [],
            index : 0,
        }
    },

    components: {
        SingleCard
    },

    created() {
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
    .then( (response) => {
        console.log(response.data.data);
        this.cardList = response.data.data;
    })
    .catch(function (error) {
        console.log(error);
    })
    },
}
</script>
<style lang="scss" scoped>
    
</style>