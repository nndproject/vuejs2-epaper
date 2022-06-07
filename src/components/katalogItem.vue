<template>
  <div>
      <ul>
          <li>
              <img class="thumbnail" alt="Gambar" :src="getImg">
              <p class="bookname">{{(index+1)+'] '+data_katalog.title}} <em>{{data_katalog.tahun}}</em></p>
          </li>
      </ul>
  </div>
</template>

<script>
export default {
    props: ['data_katalog','index'],
    computed: {
        getImg: function () {
        return require('../assets/' +this.data_katalog.gambar)
    }}
}
</script>
<!-- scope = hanya untuk halaman ini saja -->
<style scoped> 
li {
    list-style: none;
}
 .thumbnail{
     height: 240px;
 }
 .bookname{
     color: #1b1b1b;
     font-weight: 600;
 }

 em{
     font-style: normal;
     font-family: 'Courier New', Courier, monospace;
     font-size: 0.7em;
     color: red;
 }
</style>