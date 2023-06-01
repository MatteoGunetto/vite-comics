
<script>
    export default {
        name: ' CardComponents',
        props:{
            imgSrc: String,
            imgTitle: String
        }
    }
</script>
<template>
    <div class="card">
        <img :src="imgSrc" :alt="imgTitle">
        <h5>{{ imgTitle }}</h5>
    </div>
</template>

<style lang="scss">
div.card{
    width: calc(100% / 6);
    padding: 10px;
    margin-bottom: 25px;
    cursor: pointer;
    img{
        // copertine volutamente più lughe mi piangeva il cuore vederle quadrate
        width: 100%;
        height: 260px;
        object-fit: cover;
        object-position: top;
    }
    h5{
        text-transform: uppercase;
        color: white;
    }
}
</style>