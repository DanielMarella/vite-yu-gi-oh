<template>
    <div class="card pt-2 mb-4 mx-3 col-2">
        <img :src="cardImg" class="card-img-top" alt="name + 'image'">
        <div class="card-body">
            <h5 class="card-title fw-bold">
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
    .card{
        background-color: rgb(64, 255, 0);
    }
</style>