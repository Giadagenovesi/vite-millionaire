<script>
export default {
    name: "AppHeader",
}
</script>

<template>
    <header class="d-flex justify-content-center">
        <img src="../assets/img/logo.png" alt="" />   
    </header>
</template>

<style lang="scss" scoped>
header {
    height: 35%;
    padding: 1rem 0;
    background-color: #0f128d;
    img {
        max-width: 100%;
        max-height: 100%;
    }

}
</style>