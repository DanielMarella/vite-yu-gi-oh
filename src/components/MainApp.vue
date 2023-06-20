<template>
    <main>
        <CardList />
        <SelectCardType />
    </main>
</template>

<script>

import CardList from './CardList.vue';
import SelectCardType from './SelectCardType.vue';

export default {
    name : 'MainApp',
    data() {
        return {
            
        }
    },

    components : {
        CardList,
        SelectCardType,
    }
}
</script>

<style lang="scss" scoped>
    
</style>