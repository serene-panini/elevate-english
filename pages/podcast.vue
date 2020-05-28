<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="Podcast"
      image="/uploads/podcast2.png"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>Elevate English Podcast</h3>
          <p>
            <strong>This podcast is for intermediate English learners who want something interesting to listen to.</strong>
          </p>
          <p>
            I started this podcast for intermediate learners. There’s a lot of content out there to help beginners, and a ton of English media created for native speakers. 
          </p>
          <p>
           Each week I discuss topics like psychology, travel, and history to help you improve your listening comprehension. Full transcripts (written versions) of each episode are available if you want to read along while I talk.
          </p>
          <p>
            I want your opinions! If there is a topic you want me to make an episode about, use the <a href="/contact"> Contact</a> form on my website to let me know. Put "Podcast Idea" as the subject tell me about your ideas.
          </p>
          <h3>Episode Transcripts</h3>
           <p>
            <a href="/transcript-01"> Episode 01 The Psychology of Language Learning </a>
          </p>
        </div>

      <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Latest Posts
        </h3>
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
import QuoteCard from '~/components/cards/QuoteCardTwo'
export default {
  head() {
    return {
      title: `About | ${this.$siteConfig.siteName}`
    }
  },
  components: { QuoteCard }
}
</script>