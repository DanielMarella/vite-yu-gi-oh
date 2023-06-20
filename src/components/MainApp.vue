<template>
    <main>
        <SelectCardType @search="search" />
        <div class="container">
            <div class="row" v-if="store.isLoading">
                <div class="col-12">
                    <LoaderApp/>
                </div>
            </div>
            <div class="row" v-else >
                <CardList :cardList="cardList" />
            </div>
        </div>
    </main>
</template>

<script>

import CardList from './CardList.vue';
import SelectCardType from './SelectCardType.vue';
import axios from 'axios';
import LoaderApp from './LoaderApp.vue';
import {store} from '../store.js'

export default {
    name : 'MainApp',
    data() {
        return {
            store,
            cardList : [],
            apiUrl : 'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0',
        }
    },

    components : {
        CardList,
        SelectCardType,
        LoaderApp,
    },

    created() {
    this.search();
    },

    methods: {
            search(archetype_name){
                    axios.get(`${this.apiUrl}?archetype=${archetype_name}`)
                .then( (response) => {
                    this.cardList = response.data.data;
                    setTimeout( () => {
                        this.cardList = response.data.data;
                        this.store.isLoading = false;
                    },2000)
                })
                .catch(function (error) {
                    console.log(error);
                })
                }


    },
}
</script>

<style lang="scss" scoped>
    
</style>