<template>
  <NavBarComp/>
  <router-view/>
  <FooterComp/>
</template>

<script>
import NavBarComp from './components/NavBarComp.vue'
import FooterComp from './components/FooterComp.vue'

export default {
  components: {
    NavBarComp,
    FooterComp
  }
}
</script>

<style>
html{
  background-image: url(https://i.postimg.cc/h4kCb6DT/sep09.jpg);
  background-repeat: no-repeat;
  background-size: cover;
}
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
*::-webkit-scrollbar {
  display: none;
}
</style>