<template>
    <div class="background">
        <img src="../assets/spotifylogo.png" alt="Spotify Logo">
    </div>
</template>

<script>
export default {
    name: 'upperBanner',
}
</script>

<style lang="scss" scoped>
@import '../assets/commons.scss';
.background{
    background-color: $primary;
    height: 100px;
    color: white
}
img {
    width: 90px;
    padding: 15px;
}
</style>