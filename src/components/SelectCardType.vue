!<template>
    <div class="container">
        <select class="form-select w-25 mb-5" aria-label="Default select example">
            <option selected>Open this select menu</option>
            <option v-for="archetype in typeList"> {{ archetype.archetype_name}} </option>
        </select>
    </div>
</template>
<script>
import axios from 'axios';

export default {
    name : 'SelectCardType',

    data() {
        return {
            typeApiUrl : 'https://db.ygoprodeck.com/api/v7/archetypes.php',
            indexType : 5,
            typeList : [],
        }
    },


    created() {
    axios.get(this.typeApiUrl)
    .then( (type) => {
        for (let i = 0; i < 20; i++){
            this.typeList.push(type.data[i]);
        }
    })
    },

}
</script>
<style lang="scss" scoped>
    
</style>