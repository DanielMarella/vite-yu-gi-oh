<template>
    <div class="container">
        <div class="row">
            <div class="col-12">
                <h2 class="mb-5">
                    In questa pagina ci sono {{ this.cardList.length }} carte!
                </h2>
            </div>
        </div>
        <div class="row" v-if="store.isLoading">
            <div class="col-12">
                <LoaderApp/>
            </div>
        </div>
        <div class="row" v-else>
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
import LoaderApp from './LoaderApp.vue';
import axios from 'axios';
import {store} from '../store.js'
export default {
    name : 'CardList',
    data() {
        return {
            cardList : [],
            index : 0,
            store
        }
    },

    components: {
    SingleCard,
    LoaderApp
},

    created() {
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
    .then( (response) => {
        console.log(response.data.data);
        this.cardList = response.data.data;
        setTimeout( () => {
            this.cardList = response.data.data;
            this.store.isLoading = false;
        },4000)
    })
    .catch(function (error) {
        console.log(error);
    })
    },
}
</script>
<style lang="scss" scoped>
    h2{
        color: white;
    }
</style>