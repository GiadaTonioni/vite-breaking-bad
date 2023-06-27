<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import AppPokemonList from './components/AppPokemonList.vue';

import AppSearchBar from './components/AppSearchBar.vue';

import { store } from './store.js';

export default {
  components: {
    AppHeader,
    AppPokemonList,
    AppSearchBar
  },
  data() {
    return {
      store,
    }
  },
  mounted() {
    axios.get(store.apiUrl).then((response) => {
      store.pokemonList = response.data.docs;
    })
  }
}
</script>
<template lang="">
  <div>
    <AppHeader/>
    <AppSearchBar/>
    <AppPokemonList/>
  </div>
</template>

<style lang="scss">
@use './styles/generals.scss' as*;
@use './styles/partials/variables' as*;
</style>
