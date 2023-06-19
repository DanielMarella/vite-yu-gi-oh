<template>
    <header>
        <div class="head">
            <div class="logo">

            </div>
            <h1>Yu-Gi-Oh Api</h1>
        </div>
    </header>
</template>

<script>
export default {
    name : 'HeaderApp',
    data() {
        return {
            
        }
    },
}
</script>

<style lang="scss" scoped>
    
    .head{
        width: 100%;
        border: 5px solid red;
        padding: 10px 0;
        display: flex;
        align-items: center;

        .logo{
            border: 2px solid black;
            width: 80px;
            padding: 40px;
            margin: 0 10px;
        }

    }

</style>