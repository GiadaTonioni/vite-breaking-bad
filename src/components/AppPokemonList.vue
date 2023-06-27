<script>
import axios from 'axios';
import AppPokemonCard from './AppPokemonCard.vue'

export default {
    components: {
        AppPokemonCard
    },
    data() {
        return {
            pokemonList: []
        }
    },
    mounted() {
        axios.get('https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons').then((response) => {
            this.pokemonList = response.data.docs;
        })
    }
}
</script>
<template lang="">
    <div class="container">
        <div class="row">
            <div class="col back">
                <div class="container">
                    <div class="row">
                        <div v-for="(pokemon, index) in pokemonList" :key="pokemon.id" class="col-6 col-md-4">
                            <AppPokemonCard :myPokemon="pokemon" />
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
    </div>
</template>
<style lang="scss" scoped>
.back {
    background-color: rgb(199, 198, 198);
    border-radius: 30px;
    height: 700px;
    margin-top: 20px;
}
</style>