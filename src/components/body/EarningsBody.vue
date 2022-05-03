<template>
    <div class="earnings_container">
        <div class="contribution bordered">
            <div class="diagram"></div>
            <div class="info">
                <div><span class="circle" style="background: #ff914d"></span>Daily Routine</div>
                <div><span class="circle" style="background: #7ed957"></span>Tasks Completion</div>
                <div><span class="circle" style="background: #ff66c4"></span>Pomodoro</div>
                <div><span class="circle" style="background: #ff1616"></span>No-Fap</div>
            </div>
        </div>
        <div class="status">
            <div class="points bordered"><span class="boldest">{{earnedIncome}}</span> Points</div>
            <div class="income bordered">Rs. <span class="boldest">{{pointsObtained}}</span></div>
        </div>
    </div>
</template>

<script lang="ts">
import { Vue } from "vue-class-component";


export default class EarningsBody extends Vue{
    public earnedIncome : number = 32;
    public pointsObtained : number = 15;
}

</script>

<style scoped>

    .earnings_container{
        width: 100%;
        height: 100%;
        margin: 0;
        padding: 0 12px;
        box-sizing: border-box;
        font-family: 'Open Sans', cursive, sans-serif;
    }

    .circle{
        display: inline-block;
        width: 20px;
        height: 20px;
        border-radius: 100%;
        margin: 0 10px;
    }

    .bordered{
        box-sizing: border-box;
        border: 5px solid var(--border-color);
        border-radius: 20px;
    }

    .contribution{
        width: 100%;
        
        flex: 1;
        display: flex;
        flex-direction: row;
        justify-content:flex-start;
        align-items: center;
        padding: 0 12px;
        margin-top: 24px;
    }

    .diagram{
        width: 100px;
        height: 100px;
        box-sizing: border-box;
        border-radius: 100%;
        border: 10px solid var(--border-color);
    }

    .info{
        padding: 12px 16px;
    }

    .status{
        display: flex;
        margin-top: 24px;
    }

    .points, .income{
        flex: 1;
        font-weight: bold;
        font-style: italic;
        text-align: center;
    }

    .boldest{
        font-weight: 800;
        font-size: 60px;
        font-style: normal;
    }


</style>