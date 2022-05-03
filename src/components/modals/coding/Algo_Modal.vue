<template>
    <div class="algo_container">
        Hello there buddy.Algo Modal its working
    </div>
</template>

<script lang="ts">
import { Vue } from "vue-class-component";

export default class AlgoModal extends Vue{
    
}
</script>

<style scoped>
    .algo_container{
        /* width: 400px;
        height: 400px; */
        border-radius: 20px;
        border: 5px solid var(--border-color);
        
        position: fixed;
        z-index: 10;
        top: 10px;
        right: 10px;
        left: 10px;
        bottom: 10px;
    }
</style>