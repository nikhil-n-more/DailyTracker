<template>
    <div class="contentHeader">
        <coding-header v-if="this.contentShown == 'coding'"></coding-header>
        <no-fap-header v-if="this.contentShown == 'no-fap'"></no-fap-header>
        <tasks-header v-if="this.contentShown == 'tasks'"></tasks-header>
        <earnings-header v-if="this.contentShown == 'earnings'"></earnings-header>
    </div>
</template>

<script lang="ts">
import { Vue, Options } from "vue-class-component";
import CodingHeader from './heading/CodingHeader.vue';
import NoFapHeader from './heading/NoFapHeader.vue';
import TasksHeader from './heading/TasksHeader.vue';
import EarningsHeader from './heading/EarningsHeader.vue';

@Options({
    props: {
        contentShown : String
    },

    components : {
        CodingHeader,
        NoFapHeader,
        TasksHeader,
        EarningsHeader
    }
})

export default class HeadingContainer extends Vue{
    
}

</script>

<style scoped>
    .contentHeader{
        width: 100%;
        box-sizing: border-box;
        padding: 12px 8px;
        border-radius: 12px;
        border-bottom: 2px solid #c7d0d8;
        font-size: 20px;
        color: white;
        text-align: left;
    }
</style>