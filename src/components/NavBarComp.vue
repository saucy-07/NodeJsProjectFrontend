<template>
    <nav>
        <router-link to='/'>Store Logo</router-link>
        <router-link to="/src/views/ProductsView.vue">Products</router-link>
        <router-link to='/src/views/AboutView.vue'>About</router-link>
        <router-link to='/src/views/LogInView.vue'>Log In</router-link>
    </nav>
</template>

<script>
export default {
    name: 'NavBarComp'
}
</script>


<style scoped>
nav {
    background-color: crimson;
    display: flex;
    justify-content: space-evenly;
}
</style>