<template>
    <div class="skill-container">
        <h1>Skills</h1>
        <p>I have a good knowledge on these skills</p>
        <div class="list-programing-language">
            <div class="card"><img src="/public/html.png" alt="">html</div>
            <div class="card"><img src="/public/css.webp" alt="">css</div>
            <div class="card"><img src="/public/js.webp" alt="">js</div>
            <div class="card"><img src="/public/vuE JS1.jpg" alt="">vue.js</div>
            <div class="card"><img src="/public/react.png" alt="">React.js</div>
            <div class="card"><img src="/public/laravel.jpg" alt="">laravel</div>
        </div>
    </div>
</template>

<style scoped>
.skill-container{
    min-height: 80vh;
}
.list-programing-language{
    margin: 20px;
    display: flex;
    color: black;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 10px;
}
.card{
    flex: 1;
    flex-basis: 150px;
    transition: 1s all ease;
    min-height: 200px;
    border: 1px solid black;
    background-color: rgb(14, 13, 13);
    overflow: hidden;
}
.card img{
    width: 100%;
    height: 100%;
    object-fit: cover;
}
.card:hover{
    transform: scale(1.1);
    box-shadow: 0px 0px 100px blue;
}
</style>