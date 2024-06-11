<template>
  <div class="project-container">
    <h1>Project:</h1>
    <p>
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Fugiat, perferendis reiciendis.
      Tenetur laboriosam, unde dolores qui adipisci obcaecati in eaque iusto inventore! Ex fugit
      architecto aut? Provident velit quod quasi?
    </p>
    <div class="card">
      <img src="/public/source/ai.png" alt="" />
      <h3>Aivar</h3>
      <p>
        Proyek ini bertujuan untuk mengembangkan sebuah aplikasi web kalkulator yang tidak hanya
        mampu melakukan operasi aritmatika dasar tetapi juga dilengkapi dengan fitur chat bot
        berbasis kecerdasan buatan (AI). Fitur chat bot ini akan membantu pengguna dengan memberikan
        solusi untuk masalah matematika yang lebih kompleks, menjawab pertanyaan terkait matematika,
        dan memberikan bantuan umum tentang penggunaan kalkulator.
      </p>
      <div class="tecnologi">
        <b>Tecnologi: React.js, css, Groqq Api</b>
      </div>
      <a href="https://aivar-pro.vercel.app/" target="_blank">Demonstrasi &raquo;</a>
    </div>

    <div class="card">
      <img src="/public/source/dark-Ecomerce.png" alt="" />
      <h3>Dark Ecomerce</h3>
      <p>Proyek...</p>
      <div class="tecnologi">
        <b>Tecnologi: Html, Css</b>
      </div>
      <a href="https://dark-ecommerce-sand.vercel.app/" target="_blank">Demonstrasi &raquo;</a>
    </div>

    <div class="card">
      <img src="/public/html.png" alt="" />
      <h3>Artikel</h3>
      <p>Proyek artikel sederhana</p>
      <div class="tecnologi">
        <b>Tecnologi: Html, Css</b>
      </div>
      <a href="https://web-artikel-hehe-git-web2-farid-iskandars-projects.vercel.app/" target="_blank">Demonstrasi &raquo;</a>
    </div>
  </div>
</template>

<style scoped>
.card {
  margin: 20px;
  background-color: black;
  padding: 10px;
  transition: 1s;
  border-radius: 10px;
}
.card img {
  width: 100%;
  height: 200px;
  object-fit: contain;
  transition: 2s;
}
.card:hover {
  transform: scale(1.1);
  box-shadow: 0px 0px 10px aliceblue;
}
p {
  padding: 10px;
}
.tecnologi {
  padding: 10px;
}
a {
  text-decoration: none;
  color: black;
  background-color: aliceblue;
  padding: 10px;
  border-radius: 10px;
  transition: 1s;
}
a:hover {
  background-color: black;
  color: aliceblue;
  box-shadow: 0px 0px 10px aliceblue;
}
</style>
