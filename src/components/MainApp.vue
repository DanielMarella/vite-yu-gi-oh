<template>
    <main>
        <h1>
            Main
        </h1>
        <CardList />
    </main>
</template>

<script>

import CardList from './CardList.vue';


export default {
    name : 'MainApp',
    data() {
        return {
            
        }
    },

    components : {
        CardList,
    }
}
</script>

<style lang="scss" scoped>
    
</style>