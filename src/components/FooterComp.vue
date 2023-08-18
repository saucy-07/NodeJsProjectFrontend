<template>
    <footer>
        <img class="msi-logo" src="https://i.postimg.cc/wxbdjCrY/pngwing-com.png" alt="msi">
        <img class="nvidia-logo" src="https://i.postimg.cc/j5V8LXbT/Nvidia-Geforce-RTX-New-Badge-2022ihqiyiuqehfi.png" alt="nvidia-rtx">
        <img class="amd-logo" src="https://i.postimg.cc/PxNqvXf1/AMD-Ryzen-logo-svg.png" alt="amd">
        <h4>&copy;All Rights Reserved</h4>
    </footer>
</template>

<script>
export default {
    name: 'FooterComp'
}
</script>

<style scoped>
footer{
    display: flex;
    justify-content: space-evenly;
    background-color: white;
    color: black;
}
.amd-logo{
    margin-top: auto;
    margin-bottom: auto;
    width: 100px;
    height: 56.25px;
}
.nvidia-logo{
    margin-top: auto;
    margin-bottom: auto;
    width: 160px;
    height: 45px;
}
.msi-logo{
    margin-top: auto;
    margin-bottom: auto;
    width: 110px;
    height: 45px;
}
</style>