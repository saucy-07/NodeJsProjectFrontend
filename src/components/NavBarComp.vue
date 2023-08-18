<template>
    <nav>
        <router-link class="store-logo" to='/'>Store Logo</router-link>
        <div class="router-link-div">
        <router-link class="router-link" to="/src/views/ProductsView.vue">Products</router-link>
        <router-link class="router-link" to='/src/views/AboutView.vue'>About</router-link>
        <router-link class="router-link" to='/src/views/LogInView.vue'>Log In</router-link>
        </div>
    </nav>
</template>

<script>
export default {
    name: 'NavBarComp'
}
</script>


<style scoped>
*{
    font-size: 20px;
}
nav {
    background-color: rgb(55, 55, 55);
    display: flex;
    height: 50px;
    
}
.router-link{
    color: white;
    text-decoration: none;
    padding: 0px 15px 0px 0px;
}
.router-link-div{
    margin-left: auto;
    margin-top: auto;
    margin-bottom: auto;
}
.store-logo{
    color: white;
    text-decoration: none;
    margin-top: auto;
    margin-bottom: auto;
    padding: 0 0 0 15px;
}
.store-logo:active, .router-link:active, .store-logo:hover, .router-link:hover{
    color: orangered;
    text-decoration: underline;
}
</style>