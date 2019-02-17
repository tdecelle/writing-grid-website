<template>
    <div class="searchbar">
      <input type="text" placeholder="Search for Writers">
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component

export default class Searchbar extends Vue {}
</script>

<style scoped>

/* .searchbar {
  box-sizing: border-box;
  left: 50%;
  margin: -150px 0 0 -150px;
  position: absolute;
  top: 90%;
} */

.searchbar input {
  background-color: transparent;
  border: none;
  color: #555;
  font-family: 'Arvo';
  font-size: 20px;
}

.searchbar input:hover {
  outline: none;
}

/* TODO: change this for the default values */
.searchbar input::-webkit-input-placeholder {
  color: #AAA;
  box-shadow: 0px 1px 0px 0px #DDD; 
}

/* TODO: chagne these for the animation values */
.searchbar input:focus::-webkit-input-placeholder {
  color: black;
  box-shadow: 0px 1px 0px 0px black;
}

.searchbar input:focus {
  transform: scale(1);
}

</style>