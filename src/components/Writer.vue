<template>
    <div class="writer">
        <img :src=writer.imgurl alt="Writer's profile picture.">
        <div id="button" onclick="window.location='http://google.com';">
            Connect
        </div>
        <h2>{{ writer.name }} </h2>
        <h4>{{ writer.title }}</h4>
    </div>
</template>

<script lang="ts">
    import { Component, Prop, Vue } from 'vue-property-decorator';

    @Component

    export default class Writer extends Vue {
        @Prop() private writer!: object;
    }
</script>

<style scoped>
    .writer {
        text-decoration:none;
        text-align:left;
        width: 100%;
    }

    img {
        height: 50px;
        width: 50px;
        float: left;
        border-radius: 50%;
        margin: 10px;
    }
    
    #button {
        float: right;
        background-color:blue;
        color:white;
        cursor: default;
        background-color: #2b63bc;
        border-radius: 25px;
        padding: 10px;
        margin: 10px;
    }
    
    #button:hover {
        background-color: #5390ef;
    }
    
    
</style>
