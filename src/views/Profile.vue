<template>
  <div class="grid-container">
    <div class="grid-item" id="profile">
      <img alt="Profile pic" src="../assets/shrek.jpg" id="pic">
      <h2>Shrek the Ogre</h2>
      <h3>Editor for the Onion</h3>
      
      <p>Tags:</p>
      <ul id="tags">
        <li class="tag"> Business </li>
        <li class="tag"> Onions </li>
        <li class="tag"> Professional </li>
        <li class="tag"> Non-Fiction </li>
      </ul>
    </div>
    
    <div class="grid-item">
      <h2>Shrek's recent contribuitions:</h2>
      <ul id="contributions">
        <li class="contribution"> 
          <h3>Edit - New York Times Article</h3>
          Changed <font color="red">"...onions are simple."</font>
          to
          <font color="green">"...onions have many layers."</font> 
        </li>
        <li class="contribution"> 
          <h3>Blog post</h3>
          On Why I Hate Donkeys
          <p>Excerpt: Among different species, donkey dna is considered to have valuable composition in nutrients and...</p>
        </li>
        <li class="contribution"> 
          <h3>Blog post</h3>
          Farquaad - Make Duloc Great Again!
          <p>Excerpt: This proposed wall will keep the fairy tale creatures out of our lands, maintaining enough...</p>
        </li>
      </ul>
    </div>
    
  </div>
</template>

<style>
.grid-container {
  display: grid;
  grid-template-columns: auto auto auto;
  height: 600px;
}
.grid-item {
  border-radius: 25px;
  border: 2px solid rgba(0, 0, 0, 0.8);
  margin: 10px;
  font-size: 20px;
  text-align: center;
  background-color: white;
  height: 100%;
  left: 30px;
  
}

#pic{
  height: 200px;
  width: 200px;
  border-radius: 50%;
}

#profile {
  text-align:left;
  padding: 20px;
}

#tags{
  list-style-type: none;
}

.tag{
  border-radius: 10px;
  background-color: gray;
  width: 200px;
  margin:10px;
  padding:5px;
  color: white;
}

#contributions{
  list-style-type: none;
}

.contribution {
  border-radius: 10px;
  background-color: #dddddd;
  margin:10px;
  padding:5px;
  color: black;
}

p{
  text-align: left;
}

</style>