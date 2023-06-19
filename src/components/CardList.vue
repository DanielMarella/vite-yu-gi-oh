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
import axios from 'axios';
export default {
    name : 'CardList',
    data() {
        return {
            
        }
    },

    components: {
        SingleCard
    },

    created() {
    // Make a request for a user with a given ID
    axios.get('/user?ID=12345')
    .then(function (response) {
        // handle success
        console.log(response);
    })
    .catch(function (error) {
        // handle error
        console.log(error);
    })
    .finally(function () {
        // always executed
    });
    },
}
</script>
<style lang="scss" scoped>
    
</style>