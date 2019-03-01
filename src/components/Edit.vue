<template>
    <div class="edit">
        <div id="button" onclick="window.location='https://www.nytimes.com/';">
            View Site
        </div>
        <h3>{{ edit.writer }}</h3>
        Changed <p style="color:red;display: inline;">{{ edit.original }}</p> to 
        <p style="color:#18d100;display: inline;">{{ edit.new }}</p>
        
    </div>
</template>

<script lang="ts">
    import { Component, Prop, Vue } from 'vue-property-decorator';

    @Component

    export default class Edit extends Vue {
        @Prop() private edit!: object;
    }
</script>

<style scoped>
    .edit {
        text-align:left;
        padding:5px;
    }
    #button {
        float: right;
        background-color:blue;
        color:white;
        cursor: pointer;
        background-color: #2b63bc;
        border-radius: 25px;
        padding: 10px;
        margin: 10px;
    }
    
    #button:hover {
        background-color: #5390ef;
    }
</style>
