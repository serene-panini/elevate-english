<template>
  <div id="post-page" class="page-wrapper post-page">
    <site-hero :title="title" :subtitle="subtitle" :image="featureImage">
      <span
        v-if="author && $siteConfig.posts.displayAuthor"
        class="author-wrapper"
      >
        <strong>Author:</strong> {{ author }}
      </span>
      <span v-if="date" class="date-wrapper">
        <strong>Published on:</strong> {{ date }}
      </span>
    </site-hero>
    <form action='https://dictionary.cambridge.org/search/british/direct/?utm_source=widget_searchbox_source&utm_medium=widget_searchbox&utm_campaign=widget_tracking' method='post'> <table style='font-size:10px;background:#292929;border-collapse:collapse;border-spacing:0;width:150px;' > <tbody> <tr> <td colspan='2' style='padding:0;background:none;border:none;'> <a href='https://dictionary.cambridge.org/' style='display:block; background: transparent url(/external/images/freesearch/sbl.png?version=5.0.93) no-repeat 5px 6px;height:32px;'></a> </td> </tr> <tr> <td style='width:68px;background:none;border:none;padding:4px;'> <input style='width:100%;display:block;font-size:10px;padding:2px;border:none;' name='q' /> </td> <td style='width:50px;background:none;border:none;padding:0 4px 0 0;'> <input style='width:100%;display:block;font-size:10px;padding:2px;border:none;float:right;background:#d0a44c;' type='submit' value='Look it up' /> </td> </tr> </tbody> </table> </form>
    <main-section :one-column-constrained="true">
      <template v-slot:default>
        <div class="post-wrapper">
          <markdown :markdown="$store.state.content" />
          <div class="other-posts">
            <h6 class="subtitle is-size-4">
              Related Posts
            </h6>
            <!-- Related Posts -->
            <posts-grid :number="3" :category="category" :exclude="slug" />
          </div>
          <disqus-comments :identifier="$route.params.singlePost" />
        </div>
      </template>
      <template v-slot:sidebar>
        <post-sidebar />
      </template>
    </main-section>
  </div>
</template>
<script>
import { mapState } from 'vuex'
import { setPageData, getFormattedDate } from '../helper'
// import 'highlight.js/styles/github.css'
import Markdown from '~/components/Markdown'
import PostSidebar from '~/components/PostSidebar'
export default {
  components: {
    Markdown,
    PostSidebar
  },
  computed: {
    ...mapState([
      'title',
      'subtitle',
      'featureImage',
      'underSubtitle',
      'author',
      'category',
      'slug'
    ]),
    date() {
      return getFormattedDate(this.$store.state.date)
    },
    url() {
      return `${process.env.URL}/${this.$route.fullPath}`
    }
  },
  fetch({ store, params }) {
    setPageData(store, { resource: 'post', slug: params.singlePost })
  }
}
</script>
<style scoped lang="scss">
.edit-post {
  margin-bottom: 20px;
}
</style>
