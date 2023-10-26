<script>
import ButtonCounter from './ButtonCounter.vue';
import BlogPost from './BlogPost.vue';

export default {
  components: {
    ButtonCounter,
    BlogPost
  },
  data(){
    return{
      posts:[
        {id:1, title:'제목1'},
        {id:2, title:'제목2'},
        {id:3, title:'제목3'}
      ],
      postFontSize: 1
    }
  }
}
</script>

<template>
  <div class="layout">
    <h1>This is Components Basics page</h1>
    <ButtonCounter/>
    <ButtonCounter/>
    <ButtonCounter/>
    <hr>
    <h2>Blog</h2>
    <div :style="{ fontSize: postFontSize + 'em' }">
      <BlogPost
        v-for="post in posts"
        :key="post.id"
        :title="post.title"
        @enlarge-text="postFontSize += 0.1"
      />
    </div>
  </div>
</template>

