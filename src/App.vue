<script>
import axios from 'axios';
import AppTitle from './components/AppTitle.vue';
import { store } from './data/store';
import CardsList from './components/CardsList.vue';
import AppFilter from './components/AppFilter.vue';

export default {
  data() {
    return {
      store,
      isLoading: true,
    }
  },

  created() {
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=100&offset=0').then(res => {
      console.log(res)
      this.store.cards = res.data.data;
      this.isLoading = false;
    }).catch(err => {
      console.log(err)
    })

  },

  components: {
    CardsList,
    AppTitle,
    AppFilter,
  }
}

</script>

<template>
    <AppTitle></AppTitle>
    <AppFilter></AppFilter>

    <div class="container" v-if="isLoading"> 
      Loading..
    </div>

    <CardsList v-else></CardsList>

</template>

<style lang="scss">

</style>
