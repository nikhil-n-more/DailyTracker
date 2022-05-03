<template>
    <div class="bar_container">
        <div class="bar"></div>
        <span>{{completion}} %</span>
    </div>
</template>

<script lang="ts">
import { Vue, Options } from "vue-class-component";

@Options({
    props: {
        completion: Number,
        bar_color: String,
    }, 
})

export default class ProgressBar extends Vue{
    
}
</script>

<style scoped>

    .bar{
        /* content: ''; */
        width: 120px;
        height: 20px;
        background: #c7d0d8;
        display: inline-block;
        border-radius: 20px;
        margin-right: 12px;
    }
</style>