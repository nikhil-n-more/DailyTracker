<template>
    <div class="container">
        <div id="ds" ref="ds">
            <progress-block title="DS" :completion="dsCompleted" link="https://techiedelight.com/practice/?problem=TwoSum"></progress-block>
            <ds-modal v-if="this.showDSModal" ></ds-modal>
        </div>
        <div id="algos" ref="algos">
            <progress-block title="Algos" :completion="algoCompleted" link="https://techiedelight.com/practice/?problem=TwoSum"></progress-block>
            <algo-modal v-if="this.showAlgosModal"></algo-modal>
        </div>
        <div id="solved" ref="solved">
            <progress-block title="Solved" :completion="problemCompleted" link="https://techiedelight.com/practice/?problem=TwoSum"></progress-block>
            <solved-modal v-if="this.showSolvedModal"></solved-modal>
        </div>
        <div id="progress" ref="progress">
            <progress-bar :completion="hardSolved" bar_color="red"></progress-bar>
            <progress-bar :completion="mediumSolved" bar_color="red"></progress-bar>
            <progress-bar :completion="easySolved" bar_color="red"></progress-bar>
        </div>
    </div>
</template>

<script lang="ts">
import { Vue, Options} from "vue-class-component";
import ProgressBlock from '@/components/widgets/Progress.vue';
import ProgressBar from '@/components/widgets/ProgressBar.vue';
import DsModal from '@/components/modals/coding/DS_Modal.vue';
import AlgoModal from '@/components/modals/coding/Algo_Modal.vue';
import SolvedModal from '@/components/modals/coding/Solved_Modal.vue';

@Options({
    components: {
        ProgressBlock,
        ProgressBar,
        DsModal,
        AlgoModal,
        SolvedModal
    },
})

export default class CodingBody extends Vue{
    public dsCompleted : number = 67;
    public algoCompleted : number = 87;
    public problemCompleted : number = 43;

    public hardSolved : number = 67;
    public mediumSolved : number = 67;
    public easySolved : number = 67;

    public showDSModal : boolean = false;
    public showAlgosModal : boolean = false;
    public showSolvedModal : boolean = false;

    public $refs : Vue['$refs'] = {
        "ds" : HTMLDivElement,
        "algos" : HTMLDivElement,
        "solved" : HTMLDivElement,
        "progress" : HTMLDivElement
    }

    public mounted() : void{
        this.$refs["ds"].addEventListener('click' , () => {
        //   alert("DS trigger working perfectly");
            this.showDSModal = true;
        });

        this.$refs["algos"].addEventListener('click' , () => {
        //   alert("Algos trigger working perfectly");
            this.showAlgosModal = true;
        });

        this.$refs["solved"].addEventListener('click' , () => {
        //   alert("Solved trigger working perfectly");
            this.showSolvedModal = true;
        });

        // this.$refs["progress"].addEventListener('click' , () => {
        //   alert("Progress trigger working perfectly");
        // });
    }

}

</script>

<style scoped>

    .container{
        display: grid;
        grid-template-columns: 190px 190px;
        grid-template-rows: 120px 120px;
        box-sizing: border-box;
        padding-top: 50px;
        padding-left: 8px;
    }

    #ds, #algos, #solved, #progress{
        box-sizing: border-box;
        border: 5px solid var(--border-color);
        border-radius: 20px;
    }

    #progress{
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
    }
</style>