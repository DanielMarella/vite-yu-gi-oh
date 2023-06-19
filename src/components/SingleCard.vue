<template>
    <div class="card mb-3 col-3">
        <img :src="cardImg" class="card-img-top" alt="name + 'image'">
        <div class="card-body">
            <h5 class="card-title">
                {{cardName}}
            </h5>
            <p class="card-text">
                {{cardType}}
            </p>
        </div>
    </div>
</template>
<script>
export default {
    name : 'SingleCard',
    data() {
        return {
            
        }
    },

    props : {
        cardImg : String,
        cardName : String,
        cardType : String,
    },
}
</script>
<style lang="scss" scoped>
    
</style>