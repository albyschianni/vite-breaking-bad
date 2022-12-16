<script>
import { store } from '../store.js';
export default{
    name:"CmdSelector",
    data(){
        return {
            store,
        }
    }
}
</script>

<template>
  
    <div>
        <select v-model="store.selected" @change="$emit('ricerca')">
            <option selected value="Starter">All</option>
            <option value="Alive">Alive</option>
            <option value="Dead">Dead</option>
            <option value="Unknown">Unknown</option>
        </select>
    </div>

</template>

<style lang="scss" scoped>

select {
    width: 100px;
    margin-bottom: 40px;
    
}

</style>
