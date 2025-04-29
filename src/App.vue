<script setup>
const produtos = [
    {
        id: 1,
        titulo: 'Chain of Iron: Volume 2',
        autora: 'Cassandra Clare',
        preco: 23.24,
        capa: 'https://cdn.kobo.com/book-images/6db37b19-2d7d-4e5b-a1d8-b006188c9db4/1200/1200/False/the-last-hours-chain-of-iron.jpg',
    },
    {
        id: 2,
        titulo: 'Chain of Thorns',
        autora: 'Cassandra Clare',
        preco: 23.24,
        capa: 'https://cdn.kobo.com/book-images/4aa958d8-c1ed-4bf2-90ce-fef019f92a15/353/569/90/False/the-last-hours-chain-of-thorns.jpg',
    },
    {
        id: 3,
        titulo: 'City of Fallen Angels',
        autora: 'Cassandra Clare',
        preco: 13.94,
        capa: 'https://m.media-amazon.com/images/I/815MzJpG6iL._AC_UF1000,1000_QL80_.jpg',
    },
    {
        id: 4,
        titulo: 'Nona the Ninth',
        autora: 'Cassandra Clare',
        preco: 16.84,
        capa: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcThSjYxA73VNaIFSItXwUsuMHkRQo7f8PXGBg&s',
    },
    {
        id: 5,
        titulo: 'Harlem Shuffle',
        autora: 'Colson Whitehead',
        preco: 26.92,
        capa: 'https://m.media-amazon.com/images/I/81ZPFCh0xML.jpg',
    },
    {
        id: 6,
        titulo: 'Two Old Women',
        autora: 'Velma Wallis',
        preco: 13.95,
        capa: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQBXEMa4hM454G7Whh7PrDN8R_oYebpPdFl_Q&s',
    },
    {
        id: 7,
        titulo: 'Carrie Soto Is Back',
        autora: 'Taylor Jenkins Reid',
        preco: 26.04,
        capa: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQGJROWBwFV4AHVxK1H0NNVTiEBBlVbmnf2gg&s',
    },
    {
        id: 8,
        titulo: 'Book Lovers',
        autora: 'Emily Henry',
        preco: 15.81,
        capa: 'https://m.media-amazon.com/images/I/71Xy4AL7jKL.jpg',
    }
];
</script>

<template>
  <header>
    <div id="d1">
      <p id="p1"><a href="">IFBooks</a></p>
      <p id="p2">
        Apreço a <br> leitura
      </p>
    </div>
    <div id="d2">
      <input type="search" name="site-search" id="" placeholder="Pesquisar">
      <span class="fa-solid fa-magnifying-glass"></span>
    </div>
    <nav>
      <ul>
        <li><a href="">Termos</a></li>
        <li><a href="">Equipe</a></li>
        <li><a href="">Envio</a></li>
        <li><a href="">Devoluções</a></li>
      </ul>
    </nav>
    <nav id="icons">
      <span id="sp1" class="fa-solid fa-cart-shopping"></span>
      <span id="sp2" class="fa-solid fa-heart"></span>
      <span id="sp3" class="fa-solid fa-user"></span>
    </nav>
  </header>
  <section id="s1">
    <div>
      <button id="b1">Autor de abril</button>
      <h1>Eric-Emanuel Schmitt</h1>
      <p id="p3">
        Eric-Emmanuel Schmitt has been awarded more than 20 <br> literary prizes and distinctions, and in 2001 he received the <br> title of Chevalier des Arts et des Lettres. His books have been <br> translated into over 40 languages.
      </p>
      <button id="b2">Acessar página do livro</button>
    </div>
    <img src="../public/imgs/livro.png" alt="Livro" width="447px" height="600px">
  </section>
  <section id="s2">
    <div>
      <span class="fa-solid fa-truck"></span>
      <p>Frete grátis para SC</p>
    </div>
    <div id="d3">
      <span class="fa-solid fa-star"></span>
      <p>Livros recomendados</p>
    </div>
    <div>
      <span class="fa-solid fa-book-open"></span>
      <p id="p4">Mais vendidos</p>
    </div>
  </section>
  <section id="s3">
  <h1>Lançamentos</h1>
  <div id="livros-container">
    <div v-for="produto in produtos" :key="produto.id" id="livros">
      <img :src="produto.capa" alt="Capa do Livro" width="300px" height="474px" />
      <h2>{{ produto.titulo }}</h2>
      <p>{{ produto.autora }}</p>
      <p id="p5">R$ {{ produto.preco.toFixed(2) }}
        <span id="sp4" class="fa-solid fa-heart"></span> 
      </p>
      <button>
        <span class="fa-solid fa-cart-shopping"></span>
        <p>Comprar</p>
      </button>      
    </div>
  </div>
</section>

  <footer>
    <div id="d5">
      <div>
      <p>IFBooks</p>
      <div>
        <span id="span1" class="fa-brands fa-square-facebook"><a href=""></a></span>
        <span id="span2" class="fa-brands fa-square-instagram"><a href=""></a></span>
        <span id="span3" class="fa-brands fa-square-twitter"><a href=""></a></span>
      </div>
    </div>
    <div>
      <ul>
        <li id="l1">Contatos</li>
        <li>
          <span class="fa-solid fa-phone"></span>
          +55 47 40045263
        </li>
        <li>
          <span class="fa-solid fa-clock"></span>
          8h às 23h - Seg a Sex
        </li>
        <li>
          <span class="fa-solid fa-envelope"></span>
          contato@ifbooks.com
        </li>
      </ul>
      <div id="d4">
        <img id="im1" src="../public/imgs/paypal.png" alt="Paypal logo">
        <img src="../public/imgs/mastercard.png" alt="MasterCard logo">
        <img src="../public/imgs/visa.png" alt="Visa logo">
      </div>
    </div>
    </div>
    <p id="p6">© Alguns direitos reservados. IFbooks 2025. </p>
  </footer>
</template>

<style scoped>
header {
  display: flex;
  margin: 1vw 0 0 0;
  justify-content: space-evenly;
  align-items: center;
  border-bottom: #27AE60 1px solid;
  padding: 0 0 0.5vw 0vw;
}

#d1 {
  display: flex;
  align-items: center;
}

#p1 {
  font-weight: bold;
  font-size: 1.2rem;
  border-right: 2px solid #27AE60;
  padding: 5px 0.5vw 5px 0vw;
}

#p1 a {
  text-decoration: none;
}

#p2 {
  padding: 0 5vw 0 0.5vw;
  color: #27AE60;
}

#d2 span {
  color: #231F2D;
}

#d2 {
  position: relative;
  width: 500px;
}

#d2 input {
  width: 100%;
  padding: 10px 40px 10px 15px; 
  background-color: #F1F1F1;
  border: none;
  font-size: 15px;
  border-radius: 3px;
}

#d2 input::placeholder {
  color: #B8B8B8;
  text-align: left;
}

#d2 span {
  position: absolute;
  right: 15px;
  top: 50%;
  transform: translateY(-50%);
  color: #231F2D;
  pointer-events: none;
}

nav ul {
  display: flex;
}

nav ul li {
  list-style: none;
  margin: 0 2.5vw 0 0;
}

nav ul li a {
  text-decoration: none;
  color: #7B7881;
}

#icons span {
  color: #27AE60;
  margin: 0 1vw 0 0;
}

#sp1, #sp2 {
  border-right: 1px solid #27AE60;
  padding: 0 1vw 0 0;
  font-size: 1rem;
}

#sp3 {
  font-size: 1rem;
}

#s1 {
  display: flex;
  justify-content: space-evenly;
  border-bottom: #27AE60 1px solid;
}

#s1 div {
  width: 500px;
  padding: 3vw 0 0 0;
}

#b1 {
  background-color: transparent;
  border: #27AE60 1px solid;
  border-radius: 3px;
  color: #27AE60;
  margin: 5vw 0 1.5vw 0;
  padding: 15px 10px;
  cursor: pointer;
}

h1 {
  font-weight: bold;
  font-size: 2.8rem;
  color: #382C2C;
  margin: 0 0 1.5vw 0;
}

#p3 {
  color: #4D4C4C;
  margin: 0 0 1.5vw 0;
}

#b2 {
  background-color: #27AE60;
  border: none;
  padding: 15px 30px;
  color: white;
  border-radius: 3px;
  font-size: 0.9rem;
  cursor: pointer;
}

#s2 {
  display: flex;
  justify-content: space-around;
  align-items: center;
  gap: 20px;
  padding: 100px;
  border-bottom: 1px #27ae60 solid;
}

#s2 div {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 20px;
  padding: 20px;
}

#s2 div p, span {
  font-size: 30px;
  font-weight: bold;
  color: #382c2c;
}

#d3 {
  border-left: 1px solid;
  border-right: 1px solid;
  padding: 20px;
  width: 650px;
}

#p4 {
  border-bottom:#382C2C 1px solid;
  padding: 0 30px 0 0;
}

#s3 h1 {
  color: #231F2D;
  font-size: 2.5rem;
  margin: 0 12vw 3vw;
}

#s3 {
  padding: 40px 20px;
}

#p5 {
  font-size: 1.1rem;
  font-weight: bold;
}

#livros-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
  max-width: 1550px;
  margin: 0 auto;
}

#livros {
  flex: 1 0 21%; 
  max-width: 21%; 
  margin: 0 0 0 1vw;
  margin-bottom: 40px;
}

#livros button {
  display: flex;
  background-color: #27AE60;
  border: none;
  color: white;
  border-radius: 2px;
  font-size: 1rem;
  padding: 10px 105px;
  cursor: pointer;
  margin: 1vw 0 0 0;
}

#livros button span {
  color: white;
  padding: 0 10px 0 0;
  align-items: center;
  font-size: 1rem;
}

#sp4 {
  color: #27AE60;
  font-size: 1.5rem;
  padding: 0 0 0 10vw;
  align-items: center;
  cursor: pointer;
}

footer {
  background-color: #27AE60;
  color: white;
}

#d5 {
  display: flex;
  justify-content: space-between;
  border-bottom: 1px solid white;
  padding: 2vw 5vw;
}

footer div div span {
  color: white;
  padding: 10px 20px 0 0;
}

footer ul {
  margin: 0 0 2vw 0;
}

footer ul li {
  list-style: none;
}

footer ul li {
  padding: 0 0 0.7vw 0;
}

footer ul li span {
  color: white;
  font-size: 1rem;
  padding: 0 10px 0 0;
}

#l1 {
  font-weight: bold;
  padding: 0 0 1vw 0;
}

#d4 {
  margin: 0 0 0 2vw;
}

#d4 img {
  width: 50px;
  height: 40px;
}

#im1 {
  padding: 3px;
}

#p6 {
  align-items: center;
  display: flex;
  justify-content: center;
  padding: 1vw 0 0 0;
}
</style>