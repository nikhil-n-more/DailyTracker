<template>
    <div class="container">
        <span>Coding</span>
        <div class="progress" title="See your progress" ref="progress"></div>
        <div class="edit" title="Edit your goal" ref="edit"></div>
        <div class="reset" title="Reset your progress" ref="reset"></div>
    </div>
</template>

<script lang="ts">
import { Vue } from "vue-class-component";


export default class CodingHeader extends Vue{
    public $refs : Vue['$refs'] = {
        "progress" : HTMLDivElement,
        "edit" : HTMLDivElement,
        "reset" : HTMLDivElement
    };

    public mounted() : void{
        this.$refs["progress"].addEventListener('click' , () => {
          alert("Progress trigger working perfectly");
        });

        this.$refs["edit"].addEventListener('click' , () => {
          alert("Edit trigger working perfectly");
        });

        this.$refs["reset"].addEventListener('click' , () => {
          alert("Reset trigger working perfectly");
        });
    }
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

    .progress, .edit, .reset{
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

    .reset{
        background: #ff1616;
    }
</style>