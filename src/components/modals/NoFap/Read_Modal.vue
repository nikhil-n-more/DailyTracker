<template>
    <div class="read_container">
        Hello there buddy.Read Modal its working
    </div>
</template>

<script lang="ts">
import { Vue } from "vue-class-component";

export default class ReadModal extends Vue{
    
}
</script>

<style scoped>
    .read_container{
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