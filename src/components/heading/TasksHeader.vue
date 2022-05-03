<template>
    <div class="container">
        <span>Tasks</span>
        <div class="progress" title="See your progress"></div>
        <div class="edit" title="Edit your goal/tasks"></div>
        <div class="remaining" title="See remaining tasks"></div>
    </div>
</template>

<script lang="ts">
import { Vue } from "vue-class-component";


export default class TasksHeader extends Vue{
    
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

    .progress, .edit, .remaining{
        width: 25px;
        height: 25px;
        border-radius: 100%;
        margin-right: 8px;
        box-sizing: border-box;
    }

    .progress{
        background: #38bd71;
    }

    .edit{
        background: #38b6ff;
    }

    .remaining{
        background: #ff1616;
    }
</style>