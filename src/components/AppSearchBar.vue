<script>
import { store } from '../store.js';

export default {
    data() {
        return {
            store,
            pokemonTypeValues: [
                {
                    'type1': 'Grass',
                    'type1': 'Fire',
                    'type1': 'Water'
                }
            ]
        }
    }
}
</script>
<template lang="">
    <div class="container">
        <div class="row">
            <div class="col-12">
                <select class="form-control" v-model="store.typeValue">
                    <option value="" selected>Select type</option>
                    <option v-for="(type, index) in pokemonTypeValues" :key="index" :value="type1">{{type1}}</option>
                </select>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped></style>