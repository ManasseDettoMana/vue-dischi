<template>
    <header>
        <div class="my_container">
            <div class="row">
                <div class="col-6">
                <!-- <img src="img/spoti-logo.png" alt=""> -->
                </div>
                <div class="col-6 d-flex  align-items-center">
                    <input type="text" placeholder="inizia una ricerca" @keyup="ricercaAlbum">     
                </div>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header',
    methods:{
        // ricercaAlbum: (()=>{
        //     if(){

        //     }
        // })
    }
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

        input{
            width: 50%;
            height: 35px;
        }
    }
}

</style>