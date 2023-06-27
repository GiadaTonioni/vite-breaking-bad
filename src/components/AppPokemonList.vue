<script>
import AppPokemonCard from './AppPokemonCard.vue'
import { store } from '../store.js'

export default {
    components: {
        AppPokemonCard
    },
    data() {
        return {
            store
        }
    }
}
</script>
<template lang="">
    <div class="container">
        <div class="row">
            <div class="col back">
                <div class="container backgr">
                    <div class="row">
                        <div v-for="(pokemon, index) in store.pokemonList" :key="pokemon.id" class="col-3">
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

.backgr {
    background-color: rgb(73, 72, 72);
}
</style>