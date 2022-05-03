<template>
<div class="nofap-container">
    <div class="timer">12:36:34</div>
    <div class="report">
        <counter :count="dayCount" label="Days" style="background: #38b6ff"></counter>
        <counter :count="relapseCount" label="Relapse" style="background: #ff1616"></counter>
    </div>
    <div class="activity">
        <div class="progress">{{readingProgress}}%</div>
        <div class="info">
            <p class="status">Reading</p>
            <a class="book_name" href="#">{{currentBook}}</a>
        </div>
    </div>
</div>
</template>

<script lang="ts">
import { Vue, Options } from "vue-class-component";
import Counter from '@/components/widgets/Counter.vue';

@Options({
    components: {
        Counter
    }
})

export default class NoFapBody extends Vue{
    public dayCount : Number = 7;
    public relapseCount : Number = 2;

    public readingProgress : number = 67;
    public currentBook : string = "Atomic Habbits";
}

</script>

<style scoped>
    .nofap-container{
        font-family: 'Open Sans', cursive, sans-serif;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        width: 100%;
        height: 100%;
        padding: 0;
        
    }
    .timer{
        width: 100%;
        box-sizing: border-box;
        text-align: end;
        padding: 12px;
    }
    .report{
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
    }
    .nofap-container .activity{
        width: 100%;
        box-sizing: border-box;
        border: 5px solid var(--border-color);
        border-radius: 20px;
        flex: 4;

        display: flex;
        flex-direction: row;
        justify-content:flex-start;
        align-items: center;

        margin-top: 24px;
    }

    .progress{
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

    .status{
        font-style: italic;
        font-weight: bold;
    }
    .book_name{
        font-weight: bold;
        color: #ff5757;
        font-size: 32px;
        text-decoration: none;
    }
</style>