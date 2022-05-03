<template>
    <div class="pcontainer">
        <div class="percentage">
            <div>{{completion}} %</div>
        </div>
        <div class="info">
            <div class="title"> {{title}} </div>
            <div class="link"><a :href="link" target="_blank"><i class="fa-solid fa-location-arrow"></i></a></div>
        </div>
    </div>
</template>

<script lang="ts">

import { Vue, Options } from "vue-class-component";

@Options({
    props : {
        title : String,
        completion : Number,
        link : String,
    },
})

export default class ProgressBlock extends Vue {
    
}
</script>

<style scoped>
.pcontainer{
    width: 100%;
    height: 100%;
    color: white;
    display: flex;
    overflow: hidden;
    justify-content: center;
    margin: 0;
    padding: 0;
    font-size: 40px;
}

.percentage, .info{
    flex: 1;
}

.percentage{
    display: flex;
    justify-content: center;
    align-items: center;
    box-sizing: border-box;
}

.percentage div{
    display: flex;
    justify-content: center;
    align-items: center;
    box-sizing: border-box;
    width: 80px;
    height: 80px;
    border: 10px solid #c7d0d8;
    border-radius: 100%;
    font-size: 24px;
}

.info{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

.link{
    z-index: 2;
}

.link a{
    color: #c7d0d8;
}
</style>