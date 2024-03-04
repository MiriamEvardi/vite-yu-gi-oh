<script>
import CardItem from './CardItem.vue';
import AppCount from './AppCount.vue';

import {store} from '../data/store.js';

export default {
  name: 'CardsList',
 
      components: {
        CardItem,
        AppCount
      },
    
      data() {
        return {
          store,
      }
    },


}
</script>

<template>
  
  <div class="container">
    <select>
      <option>Option 1</option>
      <option>Option 2</option>
      <option>Option 3</option>
      <option>Option 4</option>
      <option>Option 5</option>
    </select>
  
   
      <AppCount></AppCount>
      <ul>
        <CardItem v-for=" currentCard in store.cards" 
        :card="currentCard">

        </CardItem>
      </ul>
    
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
   border-top: 0;
    
  }
</style>
