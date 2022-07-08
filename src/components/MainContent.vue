<template>
    
    <div class="background">
        <div class="container">
            <div class="row">
                <div class="col-12 d-flex justify-content-evenly flex-wrap">

                    <div v-if="isLoadin">
                        <div class="loader">
                            <h2>LOADING TRACKS..</h2>
                        </div>
                    </div>

                    <div v-else v-for="item, index in dataList" :key="index">
                        <singleTrack :info="dataList" :item="item" />
                    </div>

                </div>
            </div>
        </div>
    </div>

</template>

<script>
import axios from 'axios';
import singleTrack from './singleTrack';
export default {
    name: "MainContent",
    data() {
        return {
            url: "https://flynn.boolean.careers/exercises/api/array/music",
            dataList: [],
            isLoadin: true,
        };
    },
    created() {
        this.getData();
    },
    methods: {
        getData() {
            axios.get(this.url).then((result) => {
                this.dataList = result.data.response;
                setTimeout(() => {
                    this.isLoadin = false;
                }, 1000);
            });
        }
    },
    components: { singleTrack }
}
</script>


<style lang="scss" scoped>
@import '../assets/commons.scss';
.background{
    background-color: $main-color;
    padding: 4rem;
    color: white;
}
h2 {
    font-size: 40px;
    color: white;
}
</style>