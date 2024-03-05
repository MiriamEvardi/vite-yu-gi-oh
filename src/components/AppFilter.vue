<script>
import {store} from '../data/store.js';


export default {

  data() {
    return {
      store,
    }
  },


}

</script>

<template>
    <div class="container">
        <select v-model="store.filterText" @change="$emit('filter')">
          <option value="0"> Filtra archetipo</option>
          <option v-for="archetype in store.archetypes" :value="archetype.archetype_name">{{ archetype.archetype_name }}
      </option>
        </select>
    </div>  
   
</template>

<style lang="scss">
@use '../style.scss' as *;

select {
  padding: 10px 20px;
  margin-bottom: 20px;

  border-radius: 10px;

  font-size: 18px;
}

</style>
