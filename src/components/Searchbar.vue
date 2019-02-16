<template>
    <div class="searchbar">
      <input type="text" placeholder="Search for Writers">
      <span class="underline"></span>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component

export default class Searchbar extends Vue {}
</script>

<style scoped>

.searchbar {
  background-color: #FF0;
  border-radius: 2px;
  box-shadow: 0px 2px 1px 0px #DDD;
  width: 300px;
  margin: auto;
  width: 50%;
}

.searchbar input {
  background-color: transparent;
  border: none;
  border-bottom: 1px solid #CCC;
  color: #555;
  box-sizing: border-box;
  font-family: 'Arvo';
  font-size: 18px;
  margin: auto;
  width: 50%;
  top: 50%;
  width: 200px;
}

.searchbar input:hover {
  outline: none;
}

.searchbar input::-webkit-input-placeholder {
  color: #AAA;
}

.searchbar input:focus::-webkit-input-placeholder {
  color: dodgerblue;
}

.searchbar input:focus+.underline {
  transform: scale(1);
}

.underline {
  background-color: dodgerblue;
  display: inline-block;
  height: 2px;
  left: 50px;
  margin-top: -4px;
  top: 185px;
  -webkit-transform: scale(0, 1);
  transform: scale(0, 1);
  -webkit-transition: all 0.5s linear;
  transition: all 0.5s linear;
  width: 202px;
}

</style>