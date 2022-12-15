<script>

export default{
    name:"AppHeader",
    props: ["msg"]
}
</script>

<template>
  <header class="container">
    <h1>{{msg}}</h1>
  </header>
</template>

<style lang="scss" scoped>

h1 {
    font-weight: 700;
    text-align: center;
}
</style>
