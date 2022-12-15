<script>

export default{
    name:"SingleCharacter",
    props: ["info"]
}
</script>

<template>
  <div class="character">
        <img :src="info.image" alt="">
        <h4>{{info.name}}</h4>
        <div>{{info.status}}</div>
        <div>{{info.species}}</div>
    </div>
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
