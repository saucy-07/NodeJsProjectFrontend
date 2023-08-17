<template>
    <div class="big-div">
        <div>
        <h3>Motherboards</h3>
        <div class="image-div"></div>
    </div>
    <div>
        <h3>Graphics Cards</h3>
        <div class="image-div"></div>
    </div>
    <div>
        <h3>Processors</h3>
        <div class="image-div"></div>
    </div>
    </div>
</template>

<script>
export default {
    name: 'HomePageProductsDisplay'
}
</script>

<style scoped>
.big-div{
    background-color: violet;
    display: flex;
    justify-content: space-evenly;
}
.image-div{
    width: 150px;
    height: 100px;
    background-color: gray;
}
</style>