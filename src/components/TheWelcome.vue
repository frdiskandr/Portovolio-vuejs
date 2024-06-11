<script setup>
import { RouterLink } from 'vue-router'
import Skillview from './subcontent//SkillComponent.vue'
</script>

<template>
  <div class="container">
    <div class="introduce">
          <h1>Hi, theree..</h1>
      <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. 
        Distinctio minima qui, laboriosam sint obcaecati ex nemo ab natus sapiente,
         quidem dolorem cum eius accusantium quae. A, omnis? Sapiente, laudantium harum!</p>
       <RouterLink to="/Resume">Resume</RouterLink>
    </div>
    <div class="profile-image">
      <img src="/public/favicon.ico" alt="">
    </div>
  </div>
  <Skillview/>
</template>

<style scoped>
.container{
  display: flex;
  flex-wrap: wrap;
  min-height: 100vh;
}
.introduce{
  flex-grow: 1;
  flex-basis: 300px;
  max-width: 600px;
  justify-content: center;
  text-align: center;
  padding-top: 20em;
}
.introduce p{
  padding: 1em;
}
.introduce a{
  text-decoration: none;
  color: whitesmoke;
  background-color: blue;
  padding: 0.5em;
  border-radius: 10px;
  font-size: large;
  transition: 0.5s;
}
.introduce a:hover{
  background-color: blueviolet;
  box-shadow: 1px 1px 10px whitesmoke;
}
.profile-image{
  flex-grow: 1;
  padding: 2em;
  display: flex;
  justify-content: center;
  align-self:start;
  min-width: 400px;
  margin-top: 5em;
}
.profile-image img{
  width: 80%;
  height:80%;
  object-fit: cover;
  filter: drop-shadow(0px 0px 300px blue);
}
</style>
