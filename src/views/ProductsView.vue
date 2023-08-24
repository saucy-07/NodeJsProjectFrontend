<template>
    <h3>Products Page</h3>

    <div class="row">
            <h2 class="class-display2 text-white">Menu</h2>
        </div>
        <div class="row justify-content-center gap-3" v-if="products">
            <div class="col" v-for="product of products" :key="product">
                <div class="card" style="width: 18rem;">
                    <img :src="product.prodUrl" class="card-img-top img-fluid" :alt="product.prodName">
                    <div class="card-body">
                      <h5 class="card-title">{{ product.prodName }} <br> R {{ product.amount }}</h5>
                      <p class="card-text"><span>Category: {{ product.Category }}</span></p>
                      <!-- <button @click="singleProduct(product.prodID)">view more</button> -->
                    </div>
                  </div>
            </div>
        </div>
</template>

<script>
export default {
    name: 'ProductsView',

    computed: {
        products() {
            return this.$store.state.products
        }
    },
    mounted() {
        this.$store.dispatch('fetchProducts')
    }
}
</script>