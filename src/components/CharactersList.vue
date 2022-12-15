<script>

import SingleCharacter from './SingleCharacter.vue';

import { store } from '../store.js';

export default{
    name:"CharactersList",
    components:{
        SingleCharacter
    },
    data(){
        return{
            store,
        }
    }
}
</script>

<template>
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
