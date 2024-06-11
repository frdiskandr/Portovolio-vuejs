<script setup>
import { RouterLink } from 'vue-router'
import Skillview from './subcontent//SkillComponent.vue'
</script>

<template>
  <div class="container">
    <div class="introduce">
      <h1>Hi, theree..</h1>
      <p>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Distinctio minima qui, laboriosam
        sint obcaecati ex nemo ab natus sapiente, quidem dolorem cum eius accusantium quae. A,
        omnis? Sapiente, laudantium harum!
      </p>
      <RouterLink to="/Resume">Resume</RouterLink>
    </div>
    <div class="profile-image">
      <img src="/public/1718099505722.png" alt="" />
    </div>
  </div>
  <Skillview />
</template>

<style scoped>
.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr;
  grid-template-areas: "introduce profile-image";
  min-height: 100vh;
}
.introduce{
  grid-area: introduce;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.introduce p {
  padding: 1em;
}
.introduce a {
  text-decoration: none;
  color: whitesmoke;
  background-color: blue;
  padding: 0.5em;
  border-radius: 10px;
  font-size: large;
  transition: 0.5s;
}
.introduce a:hover {
  background-color: black;
  box-shadow: 1px 1px 10px whitesmoke;
}
.profile-image{
  grid-area: profile-image;
  display: flex;
  align-items: center;
  justify-content: center;
}
img{
  width: 100%;
  height: 100%;
  object-fit: contain;
  filter: drop-shadow(0px 0px 10px blue);
}
@media (width < 600px){
  .container{
    grid-template-columns: 1fr;
    grid-template-rows: 1fr 1fr;
    grid-template-areas: "introduce" "profile-image";
  }
}

</style>
