<template>
  <div id="app">
    
  <Header v-on:ganti-katalog="gantiKatalog"></Header>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <hr/>
    <!-- <KatalogItem v-bind:data_katalog="katalog"></KatalogItem> -->
    <article>
    <KatalogItem v-for="(item , index) in katalog" v-bind:data_katalog="item" :key="index" v-bind:index="index"></KatalogItem>
    </article>
  <Footer></Footer>
  </div>
</template>

<script>
import headerItem from './components/partial/HeaderItem.vue'
import footerItem from './components/partial/FooterItem.vue'
import KatalogItem from './components/katalogItem.vue'

export default {
  name: 'App',
  data() {
    return {
      katalog: [
        {
          id: 1,
          title: 'Katalog MobiAir',
          pdf: './assets/videotron.pdf',
          tahun: '2022',
          gambar: 'cover-mobiair.jpg'
        },
        {
          id: 2,
          title: 'Katalog MobiAir 2',
          pdf: './assets/videotron.pdf',
          tahun: '2022',
          gambar: 'cover-mobiair.jpg'
        },
      ]
    }
  },
  components: {
    Header: headerItem,
    Footer: footerItem,
    KatalogItem
  },
  methods: {
    gantiKatalog:function () {
      this.katalog.title = 'E-paper MobiAir'
    }
  },

}
</script>

<style>
#app {
  font-family: 'Jost', Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
	font-size: 18px;
	line-height: 1.44;
	word-break: break-word;
  transition-duration: 0.4s;
}

.button {
  background-color: #4CAF50; 
  border: none;
  color: white;
  padding: 10px 24px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  border-radius: 8px;
  cursor:pointer;
}
.button:hover {
  background-color: #fff; 
  color: #2c3e50;
  border: 1px solid #4CAF50; 
}

article {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  text-align: center;
}
</style>
