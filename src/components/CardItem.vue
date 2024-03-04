<script>

export default {
    name: 'CardItem',
    props: {
        card: Object,
    },

}

</script>

<template>

    <li class="card">
        <img :src="card.card_images[0].image_url" :alt="card.name" class="image">
        <div class="title">{{ card.name }}</div>
        <div>{{ card.archetype }}</div>
    </li>
  
</template>

<style lang="scss">
 .card {
    display: flex;
    flex-flow: column;
    padding-bottom: 20px;
    
    width: calc((100% / 5) - ((20px * 4) / 5));

    text-align: center;

    background-color: pink;
    color: black;

    .image {
        width: 100%;
    }

    .title {
        text-transform: uppercase;
        padding: 20px 0;
    }

 }

</style>
