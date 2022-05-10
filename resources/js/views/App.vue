<template>
  <div>
      <header>
        <nav>
          <ul>
            <li>ciao</li>
          </ul>
        </nav>
      </header>
      <PostsGrid />
      <footer>
        &copy; Boolpress
      </footer>
  </div>
</template>

<script>

  // import PostsGrid from './Posts.index.vue';
  import PostsGrid from './Posts.index.vue';


  export default {
    component:{
      PostsGrid,
    }

  }
</script>

<style>

</style>