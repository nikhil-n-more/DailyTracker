<template>
    <div class="solved_container">
        Hello there buddy.Solved Modal its working
    </div>
</template>

<script lang="ts">
import { Vue } from "vue-class-component";

export default class SolvedModal extends Vue{
    
}
</script>

<style scoped>
    .solved_container{
        /* width: 400px;
        height: 400px; */
        border-radius: 20px;
        border: 5px solid #c7d0d8;
       
        position: fixed;
        z-index: 10;
        top: 10px;
        right: 10px;
        left: 10px;
        bottom: 10px;
    }
</style>