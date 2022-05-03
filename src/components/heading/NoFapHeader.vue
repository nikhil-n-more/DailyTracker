<template>
    <div class="container">
        <span>No-Fap</span>
        <div class="motivation" title="Your moivation for nofap"></div>
        <div class="edit" title="Links to help with nofap"></div>
        <div class="relapse" title="Relapse"></div>
    </div>
</template>

<script lang="ts">
import { Vue } from "vue-class-component";


export default class NoFapHeader extends Vue{
    
}

</script>

<style scoped>

    .container{
        display: flex;
        justify-content: space-around;
    }
    
    span{
        flex: 1;
    }

    .motivation, .edit, .relapse{
        width: 25px;
        height: 25px;
        border-radius: 100%;
        margin-right: 8px;
        box-sizing: border-box;
    }

    .motivation{
        background: #38bd71;
    }

    .edit{
        background: #38b6ff;
    }

    .relapse{
        background: #ff1616;
    }
</style>