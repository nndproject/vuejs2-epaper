<template>
<header>
    <ul>
        <li>
            <a href="#">Beranda</a>
        </li>
        <li>
            <a href="#">Katalog</a>
        </li>
        <li>
            <a href="#">Kontak Kami</a>
        </li>
    </ul>
    
  <p class="title">Hi Administrator!</p>
  <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Itaque provident amet odit delectus debitis deleniti iste quam? Ab distinctio amet, ipsam accusantium nam, natus commodi quae voluptatum sequi est incidunt? Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ea nisi eaque earum animi veniam. Odit minus, ex aliquam est necessitatibus maiores hic! Ipsa ea cupiditate adipisci. Velit autem ducimus minima?</p>
  <button class="button" v-on:click="$emit('ganti-katalog')">Tambah Brosur</button>
</header>
</template>
<script>

export default ({
    setup() {
        
    },
})
</script>
<style scoped>
.title{
    font-size: 1.1em;
    font-weight: 600;
    color: #000;

}
 ul{
     list-style: none;
 }
 ul li {
     display: inline;
     padding-right: 20px;
     text-transform: uppercase;
 }
 li a{
     font-size: 1.2em;
     font-weight: 600;
     text-decoration: none;
     color: rgb(248, 31, 1);
 }
 li a:hover{
     color: black;
 }

 p{
     font-size: 0.8em;
 }
</style>