<template>
    <div class="loader-wrapper">
        <!-- <img src="http://www.mcleodgolf.com.au/wp-content/plugins/wp-restaurant-booking/images/loading.gif" alt=""> -->
        <i class="ex-10-icon fas fa-circle-notch"></i>
        <h1>Loading</h1>
    </div>
</template>

<script>
export default {
    name: 'Loader'
}
</script>

<style scoped lang="scss">

.loader-wrapper{
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    h1{
        font-size: 50px;
        font-weight: 800;
        margin-top: 50px;
        color: white;
    }
    i{
        animation: full-spin 1s linear infinite;
        font-size: 100px;
    }

    @keyframes full-spin{
        0%{
            transform: rotate(1turn);
        }
    }
}
</style>