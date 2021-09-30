<template>
    <main>
        <div class="albums_container">
            <div class="row">
                <div v-for="(element, index) in albumList" :key="index" class="album">
                    <SingleAlbum :albumItem="element"/>
                </div>
            </div>
        </div>
    </main>
</template>

<script>
import axios from 'axios';
import SingleAlbum from './SingleAlbum.vue'
export default {
    name: 'Main',
    components: {
        SingleAlbum,
    },
    data: function(){
        return{
            albumList: [],
            apiAddress: 'https://flynn.boolean.careers/exercises/api/array/music',
        }
    },
    created: function(){
        axios.get(this.apiAddress)
        .then((response) =>{
            this.albumList = response.data.response.slice();    //array copiato
            console.log(this.albumList);
        })
    }

}
</script>

<style lang="scss">
@import '../general/variables.scss';
main{
    background-color: #2b2b3d;
    height: calc(100vh - 75px);
    .albums_container{
        width: 90%;
        margin: 0 auto;
        .row{
            padding-top:100px ;
        }
        .album{
            width: calc(100% / 5 - 90px);
            background-color: $primaryGrey;
            margin: 0 20px 20px 20px;    
        }
    }
}

</style>