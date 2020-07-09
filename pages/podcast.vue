<template>
  <div id="podcast-page" class="page-wrapper about-page content-page">
    <site-hero
      title="Podcast"
      image="/uploads/podcast.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <div id="buzzsprout-player-3941621"></div>
        <script src="https://www.buzzsprout.com/1122713/3941621-the-psychology-of-language-learning.js?container_id=buzzsprout-player-3941621&player=small" type="text/javascript" charset="utf-8"></script>
        <h3>Elevate English Podcast</h3>
          <p>
            Visit the <a href="https://elevateenglishpodcast.buzzsprout.com/" target="_blank">podcast feed</a> to catch up on the most recent episodes!
          <p>
            I started this podcast for intermediate learners. There’s a lot of content out there to help beginners, and a ton of English media created for native speakers. If you find yourself in the middle, this podcast can help. 
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
          <p>
            <a href="/transcript-blue-moon"> Once in a Blue Moon </a>
          </p>
          <p>
          <a href="/transcript-02"> Episode 02 Stoicism </a>
          </p>
          
        </div>
      </template>

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