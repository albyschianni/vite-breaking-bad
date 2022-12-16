<script>
import axios from 'axios';
import SingleCharacter from './SingleCharacter.vue';
import CmdSelector from './CmdSelector.vue';

import { store } from '../store.js';

export default{
    name:"CharactersList",
    components:{
        SingleCharacter,
        CmdSelector,
    },
    data(){
        return{
            store,
        }
    },
    methods:{
    callApi(){
    let newUrl = store.apiURL;

    if ((store.selected == "Starter") || (store.selected == "")){
      newUrl
    }
    else {
      newUrl += `?status=${store.selected}`
    }
    axios
    .get(newUrl)
    .then(res =>{
      store.risultato = res.data.results
    })
    },
    }
}
</script>

<template>

    <CmdSelector @ricerca="callApi" />

  <section class="container">
    <div class="row">
        <div v-for="character in store.characterList" :key="character.id">
            <SingleCharacter :info="character" />
        </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>

.row {
    display: flex;
    flex-wrap: wrap;
    
}

</style>
