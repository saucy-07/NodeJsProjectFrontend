<template>
    <div class="hero-div">
        <h1>This is the Hero Section</h1>
    </div>
</template>

<script>
export default {
    name: 'HeroComp'
}
</script>

<style scoped>
.hero-div{
    margin: 10px auto 10px auto;
    width: 99%;
    height: 500px;
    background-image: url(https://i.postimg.cc/MHRnh9hn/wallpaperflare-com-wallpaper-1.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
    color: white;
}
h1{
    color: orangered;
}
</style>