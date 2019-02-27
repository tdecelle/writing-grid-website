<template>
    <div id="listing-item">
        <div id="button" onclick="window.location='http://google.com';">
            Apply
        </div>
        <h2>{{ listing.company }}</h2>
        <h3>{{ listing.title }}</h3>
        <p>{{ listing.pay }} - {{ listing.date }}</p>
    </div>
</template>

<script lang="ts">
    import { Component, Prop, Vue } from 'vue-property-decorator';

    @Component

    export default class Listing extends Vue {
        @Prop() private listing!: object;
    }
</script>
<style scoped>
    #listing-item {
        text-align: left;
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
