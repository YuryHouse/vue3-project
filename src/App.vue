<template>
    <div class="app">
        <post-list :posts="posts"/>
        <post-form @create="createPost"/>
    </div>
</template>

<script>
import PostList from "@/components/PostList.vue";
import PostForm from "@/components/PostForm.vue";
export default {
    components: {
        PostForm, PostList
    },
    data() {
        return {
            posts: [
                {id: 1, title: 'JS', body: 'description'},
                {id: 2, title: 'JS2', body: 'description2'},
                {id: 3, title: 'JS3', body: 'description3'},
            ],
        }
    },
    methods: {
        createPost(post) {
            this.posts.push(post);
        },
    }
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.app {
    padding: 20px;
}
</style>