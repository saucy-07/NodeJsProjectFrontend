<template>
    <div class="hero-div">
        <p class="store-logo"><i><b>BIG DADDY PC COMPANY™</b></i></p>
        <p class="slogan"><i><b>STRUGGLING TO FIND THE BEST PC DEALS?
            <br>
            DON'T WORRY... DADDY'S GOTCHA!</b></i></p>
    </div>
</template>

<script>
export default {
    name: 'HeroComp'
}
</script>

<style scoped>
.hero-div{
    margin: 10px 0 10px 0;
    width: 100%;
    height: 500px;
    background-image: url(https://i.postimg.cc/MHRnh9hn/wallpaperflare-com-wallpaper-1.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
}
.store-logo{
    margin: 0 auto 20px 20px;
    color: orangered;
    font-size: 100px;
}
.slogan{
    width: 950px;
    text-align: right;
    color: orange;
    font-size: 45px;
    margin: 225px 15px 0 auto;
}
</style>