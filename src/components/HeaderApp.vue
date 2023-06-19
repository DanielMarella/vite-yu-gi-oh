<template>
    <header>
        <div class="head mb-5">
            <div class="logo mx-3">
                <img src="../assets/logo.png" alt="logo di Yu-Gi-Oh">
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
    header{
        background-color: white;
        color: lime;

        img{
            width: 100px;
        }
    }
    .head{
        width: 100%;
        padding: 10px 0;
        display: flex;
        align-items: center;
        border-bottom: 5px solid greenyellow;
        .logo{
        }

    }

</style>