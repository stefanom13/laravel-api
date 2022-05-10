<template>
    <div>
        <div class="">
            <header>
                <h1>Ultimi Post</h1>
            </header>
        </div>
        <div class="container grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4">
            <div v-for="post in posts" :key="post.id">
                {{ post.title }}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            posts: [],
        };
    },
    // creiamo metodo fetchpost (userà axios per fare la chiamata)
    methods: {
        fetchPosts() {
            axios.get('/api/posts')
            .then( res =>{
                // console.log(res.data.posts);

                // destrutturazione
                const {posts} = res.data
                this.posts = posts
            })
            .catch( err => {
                console.warn(err);
            })
        },
    },
    mounted() {
        this.fetchPosts();
    },
    // quando il componente verrà montato invocherà questa funzione
    // Axios recupererà i dati e li salverà in ($posts=[])
};
</script>

<style></style>
