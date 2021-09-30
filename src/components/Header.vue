<template>
    <header>
        <div class="my_container">
            <div class="row">
                <!-- <img src="img/spoti-logo.png" alt=""> -->
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style scoped lang="scss">
@import '../general/variables.scss';
.my_container{
    width: 100%;
    margin: 0 auto;
    background-color:$primaryGrey;
    .row{
        height: 75px;
    }
}

</style>