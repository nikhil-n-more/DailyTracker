<template>
    <div class="task_container">
        <div class="activities">
            <div class="daily card">
                <div class="circle">{{dailyActivity}}%</div>
                <div>Daily</div>
            </div>
            <div class="tasks card">
                <div class="circle">{{tasksActivity}}%</div>
                <div>Tasks</div>
            </div>
        </div>
        <div class="meets card">
            <div class="circle">{{classActivity}}%</div>
            <div class="info">
                <p class="tag">Next Class</p>
                <a class="class_name" :href="classLink">{{nextClass}}</a>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { Vue } from "vue-class-component";


export default class TasksBody extends Vue{
    public nextClass : string = "Psychology";
    public classLink : string = "#";
    public classActivity : number = 67;
    public dailyActivity : number = 67;
    public tasksActivity : number = 67;
}

</script>

<style scoped>

    .task_container{
        box-sizing: border-box;
        width: 100%;
        height: 100%;
        margin: 0;
        padding: 12px 8px;
        font-family: 'Open Sans', cursive, sans-serif;
        font-weight: bold;
    }

    .activities{
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .daily, .tasks, .meets{
        box-sizing: border-box;
        border: 5px solid var(--border-color);
        border-radius: 20px;
    }

    .circle{
        width: 80px;
        height: 80px;
        border-radius: 100%;
        border: 10px solid var(--border-color);
        box-sizing: border-box;
        margin: 12px 16px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .card{
        width: 100%;
        box-sizing: border-box;
        border: 5px solid var(--border-color);
        border-radius: 20px;
        flex: 1;
        display: flex;
        flex-direction: row;
        justify-content:flex-start;
        align-items: center;

        margin-top: 24px;
    }

    .info{
        flex: 1;
    }

    .tag{
        font-style: italic;
        font-weight: bold;
    }

    .class_name{
        width: 100%;
        display: block;
        font-weight: 800;
        color: #db026a;
        font-size: 32px;
        text-decoration: none;
        text-align: center;
    }

</style>