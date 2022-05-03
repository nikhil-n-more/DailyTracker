<template>
    <div class="counterContainer">
        <p class="count">{{count}}</p>
        <p class="label">{{label}}</p>
    </div>
</template>

<script lang="ts">
import { Vue, Options } from "vue-class-component";

@Options({
    props: {
        count: Number,
        label: String,
    }
})

export default class Counter extends Vue{
    
}
</script>

<style scoped>
    .counterContainer{
        width: 120px;
        height: 120px;
        border: 3px solid #c7d0d8;
        border-radius: 100%;
        padding: 0;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
    }

    .count{
        font-size: 60px;
        font-weight: 800;
        margin: 0;
        padding: 0;
        /* color: #38b6ff; */
    }

    .label{
        margin-top: -8px;
        padding: 0;
    }

</style>