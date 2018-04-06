<template>
  <div id="posts">
    <PostPreview
      v-for="post in posts"
      :key="post.id"
      :excerpt="post.previewText"
      :title="post.title"
      :thumbnailImage="post.thumbnailUrl"
      :id="post.id"
    />

  </div>
</template>

<script>
import PostPreview from '~/components/Blog/PostPreview'
export default {
  components: {
    PostPreview
  },
  data() {
    return {
      posts: [
        {
          title: 'A new beginning',
          previewText: 'This is preview text',
          thumbnailUrl: 'https://source.unsplash.com/random',
          id: 'new-beginning'
        },
        {
          title: 'A sescond beginning',
          previewText: 'This is preview text',
          thumbnailUrl: 'https://source.unsplash.com/random',
          id: 'second-beginning'
        }
      ]
    };
  }
};
</script>

<style scoped>
  #posts {
    padding-top: 2rem;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }

  @media (min-width: 35rem) {
    #posts {
      flex-direction: row;
    }
  }
</style>
