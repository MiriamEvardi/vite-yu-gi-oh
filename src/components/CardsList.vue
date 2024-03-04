<script>
import AppTitle from './AppTitle.vue';
import CardItem from './CardItem.vue';

import {store} from '../data/store.js';

export default {
  name: 'CardsList',
 
      components: {
        AppTitle,
        CardItem
      },
    
      data() {
        return {
          store,
          loading: true,
      }
    },


    created() {
      setTimeout(() => {
        this.loading = false;
      },1000);
    }
}
</script>

<template>
  <AppTitle></AppTitle>
  
  <div class="container">
    <select>
      <option>Option 1</option>
      <option>Option 2</option>
      <option>Option 3</option>
      <option>Option 4</option>
      <option>Option 5</option>
    </select>
  
    <div v-if="loading" class="loader">Loading...</div>
    <div v-else>
      <ul>
        <CardItem v-for=" currentCard in store.cards" 
        :card="currentCard">

        </CardItem>
      </ul>
    </div>
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

ul {
   list-style-type: none;

   display: flex;
   flex-flow: row wrap;
   gap: 20px;

   background-color: white;
   border: solid white 40px;
    
  }
</style>
