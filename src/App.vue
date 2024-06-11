<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  
  <div class="main-conteiner">
    <div class="bacground">
      <video autoplay muted loop id="Background-video">
        <source src="/public/source/background.mp4" type="video/mp4">
      </video>
    </div>
    <div class="header">
      <div class="header-container">
        <div class="title">
          <img src="/public/favicon.ico" alt="" class="logo">
          <div class="name">
               <h1>M Faried iskandar</h1>
          <p>Frontend Developer</p>
          </div>
        </div>
        <div class="navbar">
          <ul>
            <li><RouterLink to="/">Home</RouterLink></li>
            <li><RouterLink to="/project">Project</RouterLink></li>
            <li><RouterLink to="/resume">Resume</RouterLink></li>
            <li class="Git"><a href="https://github.com/frdiskandr" target="_blank">
              <img src="/public/github_PNG40.png" alt="">
              <p>Git</p>
            </a></li>
          </ul>
        </div>
      </div>
    </div>
    <div class="main">
      <RouterView/>
    </div>
    <div class="footer">
      <p>© 2024 Portofolio. All rights reserved.</p>
    </div>
  </div>  
</template>

<style scoped>
#Background-video{
  position: fixed;
  top: 50%;
  left: 50%;
  width: 100%;
  height: 100%;
  object-fit: cover;
  transform: translate(-50%, -50%);
  z-index: -1;
}


.main-conteiner{
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto auto 60px;
  grid-template-areas: "header" "main" "footer";
  z-index: 1;
}
.header{
  grid-area: header;
  background-color: black;
  color: aliceblue;
  position: fixed;
  z-index: 1;
  width: 100%;
}
.header-container{
  width: 70%;
  margin: auto;
  display: flex;
  flex-wrap: wrap;
}
.title{
  display: flex;
  padding: 0.5em;
  align-items: end;
  flex-grow: 1;
  gap: 10px;
  min-width: 400px;
}
.title p{
  filter: drop-shadow(0px 0px 2px rgb(78, 78, 252));
}
.logo{
  width: 2rem;
  height: 2rem;
  align-self: center;
  filter: drop-shadow(0px 0px 20px rgb(78, 78, 252));
}
.navbar{
  align-content: center;

}
.navbar ul{
  flex-grow: 2;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr auto;
  list-style: none;
}
.navbar li{
  text-align: center;
  align-content: center;
}
.navbar a{
  text-decoration: none;
  color: whitesmoke;
  padding: 0.5em;
}
.navbar a:hover{
  background-color: whitesmoke;
   border-radius: 10px;
   color: black;
}
.Git{
  margin-left: 2em;
}
.Git a{
  display: flex;
  align-items: center;
  background-color: aliceblue;
   border-radius: 10px;
   color: black;
}
.Git a:hover{
  background-color: rgb(78, 78, 252);
  color: aliceblue;
  box-shadow: 1px 1px 10px whitesmoke;
}
.Git img{
  width: 20px;
  height: 20px;
}
.main{
  padding-top: 100px;
    min-height: 100vh;
    width: 70%;
    margin: auto;
  grid-area: main;
  z-index: 0;
  position: relative;
  color: aliceblue
}
.footer{
  grid-area: footer;
  color: whitesmoke;
  text-align: center;
  align-content: center;
}
</style>
