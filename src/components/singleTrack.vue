<template>
    
    <div class="my_track">

        <img :src="item.poster" :alt="item.title">

        <div class="text-center">
            <h5>{{item.title}}</h5>
            <p>{{item.author}}</p>
            <p>{{item.year}}</p>
        </div>
    </div>

</template>

<script>
export default {
    name: 'singleTrack',
    props: {
        info: Array,
        item: Object,
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/commons.scss';
.my_track {
    width: 150px;
    height: 300px;
    padding: 15px;
    background-color: $primary;
    border: none;
    margin: 3rem;
    color: white;
    img {
        width: 120px;
        margin-bottom: 15px;
    }
    p {
        color: grey;
        display: block;
    }
}
</style>
