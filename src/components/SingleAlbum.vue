<template>
    <div class="sk">
        <img :src="albumItem.poster" alt="" class="img-fluid">
        <h2>{{albumItem.title}}</h2>
        <span>{{albumItem.author}} <br><small>{{albumItem.year}}</small></span>
    </div>
</template>

<script>
export default {
    name: 'SingleAlbum',
    props: ['albumItem']
}
</script>

<style scoped lang="scss">
@import '../general/variables.scss';

img{
    width: 80%;

}

h2{
    color:white;
}
span{
    color: grey;
}

</style>