<script >
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
