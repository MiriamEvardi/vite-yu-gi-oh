<script>
export default {
    name: 'AppTitle',
   
}

</script>

<template>
    <div class="header">
        <div class="logo">
            <img src="/public/img/yu-gi-oh.png" alt="">
        </div>
        <div>
            <h1>Yu-Gi-Oh API</h1>
        </div>
    </div>
</template>

<style lang="scss">
@use '../style.scss' as *;

.header {
    display: flex;
    align-items: center;
    background-color: white;
    color: black;
    margin-bottom: 20px;
}

.logo {
    width: 120px;
    height: 100px;

    margin: 0 50px;

    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        
    }
}

 
 h1 {
    padding: 20px 0;
 }

</style>
