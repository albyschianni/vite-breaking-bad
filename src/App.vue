<script >
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import CharactersList from './components/CharactersList.vue';

import { store } from './store.js';

export default{
  name:"App",
  components: {
    AppHeader,
    CharactersList,
  },
  data(){
    return{
      store,
    }
  },
  methods: {
    getCharacters(){

      axios
      .get(store.apiURL)
      .then(res => {
        store.characterList = res.data.results;
      })
      .catch(err => {
        console.log("Errori", err);
      }
      );

    }
  },
  mounted(){
    this.getCharacters();
  }
}
</script>

<template>
  <AppHeader :msg="store.titolo" />
  <main>
    <CharactersList />
  </main>
</template>

<style lang="scss">
@use './style/general.scss';

</style>
