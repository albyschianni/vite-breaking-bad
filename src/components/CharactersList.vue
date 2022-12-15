<script>
import { store } from '../store.js';

export default{
    name:"CharactersList",
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
        <div>
            <div class="character">
                <img src="https://rickandmortyapi.com/api/character/avatar/1.jpeg" alt="">
                <h4>nome</h4>
                <div>stato</div>
                <div>specie</div>
            </div>
        </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables.scss' as *;

h4 {
    text-transform: capitalize;

    &::after {
        content:"";
        display: block;
        width: 40px;
        height: 1px;
        margin: 1rem auto;
    }

}

img {
    border-radius: 50%;
    box-shadow: 0 0 6px 3px rgba(#000, 0.15);
}

</style>
