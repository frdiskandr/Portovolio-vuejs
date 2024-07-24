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
      <nav class="navbar navbar-expand-lg navbar-dark border-bottom">
        <div class="container-fluid">
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
          data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false"
            aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
              <li class="nav-item">
                <RouterLink class="nav-link active" aria-current="page" to="/">Home</RouterLink>
              </li>
              <li class="nav-item">
                <RouterLink class="nav-link" to="/projects">Projects</RouterLink>
              </li>
              <li class="nav-item dropdown">
                <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
                  aria-expanded="false">
                  Social Media
                </a>
                <ul class="dropdown-menu">
                  <li><a class="dropdown-item" :href="linkeind" target="_blank">Linkedin</a></li>
                  <li><a class="dropdown-item" :href="ig" target="_blank">Instagram</a></li>
                  <li>
                    <hr class="dropdown-divider">
                  </li>
                  <li><a class="dropdown-item" href="#">Something else here</a></li>
                  <span class="navbar-brand" href="#">Muhammad Faried Iskandar</span>
                </ul>
              </li>
              <li class="nav-item">
                <a class="nav-link disabled" aria-disabled="false">Resume...</a>
              </li>
            </ul>
            <form class="d-flex" role="search">
              <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
              <button class="btn btn-outline-primary" type="submit">Search</button>
            </form>
          </div>
        </div>
      </nav>
    </div>
  


    <div class="main">
      <RouterView />
    </div>
    <div class="footer">
      <p>© 2024 Portofolio. All rights reserved.</p>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      ig:'https://www.instagram.com/qwfrdzy_/',
      linkeind:'https://www.linkedin.com/in/faridiskandar26'
    }
  }
}
</script>

<style scoped>
#Background-video {
  position: fixed;
  top: 50%;
  left: 50%;
  width: 100%;
  height: 100%;
  object-fit: cover;
  transform: translate(-50%, -50%);
  z-index: -1;
}


.main-conteiner {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto auto 60px;
  grid-template-areas: "header" "main" "footer";
  z-index: 1;
}

.header {
  grid-area: header;
  background-color: black;
  color: aliceblue;
  position: fixed;
  z-index: 1;
  width: 100%;
}

.header-container {
  width: 70%;
  margin: auto;
  display: flex;
  flex-wrap: wrap;
}

.title {
  display: flex;
  padding: 0.5em;
  align-items: end;
  flex-grow: 1;
  gap: 10px;
  min-width: 400px;
}

.title p {
  filter: drop-shadow(0px 0px 2px rgb(78, 78, 252));
}

.logo {
  width: 2rem;
  height: 2rem;
  align-self: center;
  filter: drop-shadow(0px 0px 20px rgb(78, 78, 252));
}

.navbar {
  align-content: center;

}

.main {
  padding-top: 100px;
  min-height: 100vh;
  width: 70%;
  margin: auto;
  grid-area: main;
  z-index: 0;
  position: relative;
  color: aliceblue
}

.footer {
  grid-area: footer;
  color: whitesmoke;
  text-align: center;
  align-content: center;
}
</style>
