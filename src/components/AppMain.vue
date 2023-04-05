<script>
import axios from 'axios';

export default {
    name: 'AppMain',
    data() {
        return {
            posts: []
        };
    },
    created() {
        axios
        .get('http://127.0.0.1:8000/api/posts')
        .then(response => {
            console.log(response.data);

            this.posts = response.data.posts.data;
        });
    }
};
</script>

<template>
    <main>
        <div class="container">
            <div class="row mb-4">
                <div class="col">
                    <h1>
                        Boolpress Frontend
                    </h1>
                </div>
            </div>
            <div class="row mb-4">
                <div v-for="post in posts" class="col-12 col-sm-4 col-md-3">
                    <div>
                        <h2>
                            {{ post.title }}
                        </h2>
                        <h4>
                            {{ post.category ? post.category.name : '-' }}
                        </h4>
                        <p>
                            {{ post.Content }}
                        </p>
                    </div>
                </div>  
            </div>
        </div>  
    </main>
</template>

<style scoped>

</style>