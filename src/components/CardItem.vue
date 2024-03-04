<script>

export default {
    name: 'CardItem',
    props: {
        card: Object,
    }
}

</script>

<template>

    <li class="card">
        <img :src="card.card_images[0].image_url" :alt="card.name" class="image">
        {{ card.name }}
    </li>
  
</template>

<style lang="scss">
 .card {
    display: flex;
    flex-flow: column;
    gap: 30px;
    
    width: calc((100% / 5) - ((20px * 4) / 5));

     text-align: center;
        .image {
            width: 100%;
     }
 }

</style>
