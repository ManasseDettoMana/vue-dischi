<template>
    <main>
        <div class="albums_container">
            <div class="row" v-if="loading">
                <div v-for="(element, index) in albumList" :key="index" class="album">
                    <SingleAlbum :albumItem="element"/>
                </div>
            </div>
            <div class="row" v-else>
                <Loader />
            </div>
        </div>
    </main>
</template>

<script>
import axios from 'axios';
import SingleAlbum from './SingleAlbum.vue';
import Loader from './Loader.vue';
export default {
    name: 'Main',
    components: {
        SingleAlbum,
        Loader,
    },
    data: function(){
        return{
            albumList: [],
            apiAddress: 'https://flynn.boolean.careers/exercises/api/array/music',
            loading : false
        }
    },
    created: function(){
        axios.get(this.apiAddress)
        .then((response) =>{
            this.albumList = response.data.response.slice();    //array copiato
            console.log(this.albumList);
        })

        setTimeout(()=>{
            this.loading = true;
        }, 1500);
    }

}
</script>

<style lang="scss">
@import '../general/variables.scss';
main{
    background-color: #2b2b3d;
    height: calc(100vh - 75px);
    .albums_container{
        width: 70%;
        margin: 0 auto;
        .row{
            padding-top:60px ;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            justify-content: space-between;
        }
        .album{
            width: calc(100% / 5 - 40px);
            height: 400px;
            background-color: $primaryGrey;
            margin: 15px 12px 0 12px;    
            padding: 30px;
            
        }
    }
}

</style>