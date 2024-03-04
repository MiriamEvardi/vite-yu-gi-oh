<script>
import {store} from '../data/store.js'

export default {
   name: 'AppCount',
   
    data() {
        return {
            store,
        }
    },
}

</script>

<template>
   <div class="count">
    Found {{ store.cards.length }} cards.
   </div>
</template>

<style lang="scss">
.count {
    border: 40px white solid;
    border-bottom: 0;
    padding: 20px 10px;
}

</style>
