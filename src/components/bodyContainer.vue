<template>
    <div class="contentBody">
        <coding-body v-if="this.contentShown == 'coding'"></coding-body>
        <no-fap-body v-if="this.contentShown == 'no-fap'"></no-fap-body>
        <tasks-body v-if="this.contentShown == 'tasks'"></tasks-body>
        <earnings-body v-if="this.contentShown == 'earnings'"></earnings-body>
    </div>
</template>

<script lang="ts">
import { Vue, Options} from "vue-class-component";
import CodingBody from '@/components/body/CodingBody.vue';
import NoFapBody from '@/components/body/NoFapBody.vue';
import TasksBody from '@/components/body/TasksBody.vue';
import EarningsBody from '@/components/body/EarningsBody.vue';

@Options({
    props : {
        contentShown : String
    },

    components : {
        CodingBody,
        NoFapBody,
        TasksBody,
        EarningsBody
    }
})

export default class BodyContainer extends Vue{
    
}

</script>

<style scoped>
    .contentBody{
        width: 100%;
        flex: 1;
        box-sizing: border-box;
        /* padding: 12px 8px; */
        border-radius: 12px;
        border: 2px solid #c7d0d8;
        font-size: 20px;
        color: white;
        text-align: left;
    }
</style>