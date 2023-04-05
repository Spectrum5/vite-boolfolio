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
        .get('http://127.0.0.1:800/api/posts')
        .then(response => {
            console.log(response.data);

            this.posts = response.data.posts.data;
        });
    }
};
</script>

<template>
    <main>
        <h1>
            Boolpress Frontend
        </h1>
        
    </main>
</template>

<style scoped>

</style>