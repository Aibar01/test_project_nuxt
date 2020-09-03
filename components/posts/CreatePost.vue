<template>
  <v-row justify="center">
    <v-dialog v-model="dialog" persistent max-width="600px">
      <template v-slot:activator="{ on, attrs }">
        <v-btn   
          color="#FBD784"
          dark
          text
          v-bind="attrs"
          v-on="on"
        >
        <v-icon>mdi-plus-box</v-icon> Add Post
        </v-btn>
      </template>
      <form @submit.prevent='createNewPost'>
          <v-card color="#0B1D26" dark>
            <v-card-title>
            <span class="headline">New Post</span>
            </v-card-title>
            <v-card-text>
            <v-container>
                <v-row>
                <v-col cols="12">
                    <v-text-field v-model="post.preview" label="Preview*" required></v-text-field>
                </v-col>
                <v-col cols="12">
                    <v-text-field v-model="post.title" label="Title*" required></v-text-field>
                </v-col>
                <v-col cols="12">
                        <v-textarea
                        v-model="post.description"
                        label="Description*"
                        hint="Hint text"
                        ></v-textarea>
                    </v-col>
                    <v-col cols="12">
                        <v-file-input @change="onFileChange" accept="image/*" label="File input"></v-file-input>
                    </v-col>
                </v-row>
            </v-container>
            <small>*indicates required field</small>
            </v-card-text>
            <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn color="#FBD784" text @click="closeForm()">Cancel</v-btn>
            <v-btn color="#FBD784" text type="submit">Add New Post</v-btn>
            </v-card-actions>
        </v-card>
      </form>
    </v-dialog>
  </v-row>
</template>

<script>
  export default {
    data: () => ({
      dialog: false,
      post: {
        preview: '',
        title: '',
        description: '',
        image: '',
      }
    }),
    methods: {
        closeForm() {
            this.dialog = false
            this.post.preview = ''
            this.post.title = ''
            this.post.description = ''
            this.post.image = ''
        },
        onFileChange(event) {
            let file = event;
            this.post.image = file;
        },
        async createNewPost() {

            this.$store.dispatch('posts/addPost', this.post)
            this.$store.dispatch('posts/setPosts')
            this.closeForm()
        }   
    }
  }
</script>