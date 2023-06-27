<script>
export default {
    props: {
        myPokemon: Object
    }
}
</script>
<template lang="">
    <div class="card">
       <img :src="myPokemon.imageUrl" class="img-fluid" :alt="myPokemon.info"> 
        <div>{{myPokemon.number}}</div>
        <h4>{{myPokemon.name}}</h4>
        <div>{{myPokemon.type1}}</div>
    </div>
</template>
<style lang="scss" scoped>
img {
    width: 40%;
    border-radius: 50%;
}

.card {
    background-color: pink;
    border-radius: 15px;
}
</style>