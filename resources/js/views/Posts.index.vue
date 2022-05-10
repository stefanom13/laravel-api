<template>
  <div>
      <header>
          <h1>Ultimi Post</h1>
      </header>
      <div class="container">
          <div v-for="post in posts" :key="post.id">
              {{ post.title }}
          </div>
      </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
            posts:[]
        }
    },
    // creiamo metodo fetchpost (userà axios per fare la chiamata)
    methods:{
        fetchPosts(){
             // Axios.get()
        }
    },
    mounted(){
        this.fetchPosts();
    }
    // quando il componente verrà montato invocherà questa funzione
    // Axios recupererà i dati e li salverà in ($posts=[])

}
</script>

<style>

</style>