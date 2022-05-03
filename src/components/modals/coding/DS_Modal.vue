<template>
    <div class="ds_container">
        <div class="name_info">Name : </div>
        <div class="link_info">Link : </div>
        <button class="submit" ref="submit">Submit</button>
    </div>
</template>

<script lang="ts">
import { Vue} from "vue-class-component";


export default class DsModal extends Vue{

}
</script>

<style scoped>
    .ds_container{
        /* width: 400px;
        height: 400px; */
        border-radius: 20px;
        border: 5px solid var(--border-color);
        background: var(--background-color);
        position: fixed;
        z-index: 10;
        top: 10px;
        right: 10px;
        left: 10px;
        bottom: 10px;
        padding: 12px 20px;
        box-sizing: border-box;
    }

    .name_info{
        width: 340px;
        min-height: 30px;
        border-radius: 20px;
        border: 3px solid var(--border-color);
        box-sizing: border-box;
    }

    .link_info{
        width: 340px;
        min-height: 30px;
        border-radius: 20px;
        border: 3px solid var(--border-color);
        box-sizing: border-box;
    }
</style>