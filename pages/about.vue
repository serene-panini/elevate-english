<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="About Us"
      image="/uploads/home.png"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>How can I learn to actually <i>speak</i> English?</h3>
          <p>
            Hi, I'm Anne. I created Elevate English after hundreds of students asked me this question. I can read, write and understand English, but I always feel blocked when speaking. What should I do? I developed a method to help English learners at all levels improve their speaking and overall language skills. This method is based on theories from psycholinguistics, learning psychology, and my experience as an ESL teacher.
          </p>
          <h3>The Elevate Method</h3>
          <p class="subtitle">
            <ol>
              <li>Learn basic words and grammar</li>
              <li>Input: Listening and Reading</li>
              <li>Output: Speaking and Writing</li>
              <li>Regular Practice</li>
            </ol>
          </p>
          <p>
            <strong>
              Read full post to learn more about the Elevate Method
            </strong>
          </p>
        </div>

        <div class="title is-ancestor">
          <div class="title is-parent">
            <article class="title is-child box">
              <figure class="image is-1by1">
                <img src="../assets/uploads/contact.jpg" width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="title is-parent">
            <article class="title is-child box">
              <p class="title">
                About Anne
              </p>
              <p class="subtitle">
                 BA Psychology, University of British Colombia
              </p>
              <p>
                I grew up in Seattle, in the United States. After high school I moved to Vancouver, Canada to study Psychology. I've loved traveling and learning languages since I was young. I got my certificate in Teaching English as a Foreign Language (TEFL) after graduation, and started traveling the world while teaching English. Six months ago I moved to France. I studied French in high school, but I didn't feel like I learned the language well with only grammar and vocabulary. Instead, I improved my French naturally by listening to podcasts, watching YouTube videos and TV shows, and by talking to new friends French, even though it was scary at first. I want to help my English students in the same way. Even if they can't move to an English speaking country, my podcasts, YouTube channel, and blog posts can help them learn English naturally at home.
              </p>
            </article>
          </div>
        </div>
        <br/>
        <quote-card/>
        
        
        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Cool Stuff We Do
              </p>
              <p class="subtitle">
                Sooo Cool
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Other Cool Things
              </p>
              <p class="subtitle">
                Just as cool
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                All the cool
              </p>
              <p class="subtitle">
                that is all
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
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
import QuoteCard from '~/components/cards/QuoteCard'
export default {
  head() {
    return {
      title: `About | ${this.$siteConfig.siteName}`
    }
  },
  components: { QuoteCard }
}
</script>