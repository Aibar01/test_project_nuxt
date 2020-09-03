<template>
  <main>
    <CreatePost />
    <v-container fill-height>
      
      <v-row v-for='(post, index) in posts' :key='post.id' class="row">
        <template v-if='index % 2 == 0'>
          
          <v-col  cols="6" class="content">
            <p class='counter'>{{ counter(index) }}</p>
            <p class="ml-4 preview-text">{{ post.preview }}</p>
            <h1 class="title-text">{{ post.title }}</h1>
            <p class="description-text">{{ post.description }}</p>
            <v-btn class="read-mode-text" text color='#FBD784'>read more <v-icon>mdi-arrow-right</v-icon></v-btn>
          </v-col>
          <v-spacer></v-spacer>
          <v-col cols="5">
            <v-img :src="post.image"></v-img>
          </v-col>
        </template>  
        <template v-else>
          <v-col cols="5">
            <v-img :src="post.image"></v-img>
          </v-col>
          <v-spacer></v-spacer>
          <v-col  cols="6" class="content">
            <p class='counter'>{{ counter(index) }}</p>
            <p class="ml-4 preview-text">{{ post.preview }}</p>
            <h1 class="title-text">{{ post.title }}</h1>
            <p class="description-text">{{ post.description }}</p>
            <v-btn class="read-mode-text" text color='#FBD784'>read more <v-icon>mdi-arrow-right</v-icon></v-btn>
          </v-col>
        </template>  
      </v-row>
    </v-container>
    <Footer />  
  </main>
</template>

<script>
import Footer from '~/components/parts/Footer.vue'
import CreatePost from '~/components/posts/CreatePost.vue'

export default {
  mounted() {
    this.$store.dispatch('posts/setPosts')
  },
  computed: {
    posts() {
      return this.$store.getters['posts/getPosts']
    }
  },
  methods: {
    counter(counter) {
      return (counter + 1 > 10) ? counter + 1 : `0${counter + 1}`
    }
  },
  components: {
    Footer,
    CreatePost
  }
}
</script>

<style>
  main {
    position: absolute;
    top: 155%;
    width: 100%;
    background: #0B1D26;
  }
  
  .counter {
    position: absolute;

    
    font-family: 'Khula', sans-serif;
    font-weight: bold;
    font-size: 240px;
    line-height: 240px;
    
    color: #FFFFFF;

    opacity: 0.1;
  }

  .row  {
    margin-bottom: 50px;
    
  }

  .preview-text {
    margin-top: 80px;
    font-family: 'Khula', sans-serif;
    font-style: normal;
    font-weight: 800;
    font-size: 100%;
    line-height: 22px;
    
    letter-spacing: 6px;
    text-transform: uppercase;

    color: #FBD784;
  }

  .title-text {
    width: 100%;

    padding-top: 30px;
    font-family: 'Bentham', serif;
    font-weight: 600;
    font-size: 500%;
    line-height: 100px;

    text-transform: capitalize;

    color: #FFFFFF;

    flex: none;
    align-self: center;
    margin: 0px 32px;
  }

  .description-text {
    font-family: 'Khula', sans-serif;
    font-style: normal;
    font-weight: bold;
    font-size: 18px;
    line-height: 32px;
    /* or 178% */


    color: #FFFFFF;


    /* Inside Auto Layout */

    flex: none;
    order: 2;
    align-self: center;
    margin: 0px 27px;
  }

  .content {
    margin-bottom: auto;
  }

  .read-mode-text {
    font-family: 'Khula', sans-serif;
    color: #FBD784;
  }
</style>
