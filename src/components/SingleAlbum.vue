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

h2{
    color:white;
    margin-top: 14px;
    font-weight: 500;
}
span{
    color: grey;
    margin-top: 50px;

}

</style>