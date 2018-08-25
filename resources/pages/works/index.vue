<template>
  <section class="container uk-height-viewport uk-padding-large">

    <h3 class="secondary-color uk-text-center head">list of my works</h3>

    <div class="projects uk-grid-large uk-child-width-1-3@s" uk-grid>
      <div class="project" v-for="(project, index) in projects" :key="project.title" :class="`project-${index}`">
        <i class="title uk-text-strong uk-display-block" :class="`title-${index}`">
          <b>{{ project.title }}</b>
        </i>
        <p class="para" :class="`para-${index}`">{{ project.para }}</p>
        <a href="#" class="link readmore uk-display-block uk-float-right uk-text-primary" :class="`link-${index}`" @click.prevent="readMore">
          <i>{{ project.link }}</i>
          <span uk-icon="icon: arrow-right;"></span>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {

  data() {
    return {
      projects: [
        {
          title: 'school managemet system',
          para: ' Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quae quis cupiditate, fugit ullam vitae quas?',
          link: 'view more details',
        },
        {
          title: 'school managemet system',
          para: ' Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quae quis cupiditate, fugit ullam vitae quas?',
          link: 'view more details',
        },
        {
          title: 'school managemet system',
          para: ' Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quae quis cupiditate, fugit ullam vitae quas?',
          link: 'view more details',
        },
        {
          title: 'school managemet system',
          para: ' Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quae quis cupiditate, fugit ullam vitae quas?',
          link: 'view more details',
        },
        {
          title: 'school managemet system',
          para: ' Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quae quis cupiditate, fugit ullam vitae quas?',
          link: 'view more details',
        },
        {
          title: 'school managemet system',
          para: ' Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quae quis cupiditate, fugit ullam vitae quas?',
          link: 'view more details',
        }
      ]
    }
  },
  mounted() {
    this.gsanime();
  },

  methods: {
    readMore() {
      console.log('DONE');
    },

    gsanime() {
      // Create a new Timeline (equivalent to new TimelineMax())
      const tl = new this.$gsap.TimelineMax();
      // Element To Animate
      const $ = document.querySelector.bind(document);

      const head = $('.head');
      const projects = $('.projects');
      // const para = $('.para-0');
      // const link = $('.link-0');

      // const title1 = $('.title-1');
      // const para1 = $('.para-1');
      // const link1 = $('.link-1');
      

      tl
        .from(head, 0.5, { y: 50, ease: this.$gsap.Power2.easeOut })
        .from(projects, 0.5, { y: 50, autoAlpha: 0,  ease: this.$gsap.Power3.easeOut })
        // .from(project, 0.250, { y: 30, autoAlpha: 0 })
        // .from(title, 0.250, { y: 15, autoAlpha: 0 })
        // .from(para, 0.200, { y: 15, autoAlpha: 0 })
        // .from(link, 0.150, { y: 15, autoAlpha: 0 })

        // .from(title1, 0.250, { y: 15, autoAlpha: 0 }, '-=0.200')
        // .from(para1, 0.200, { y: 15, autoAlpha: 0 })
        // .from(link1, 0.150, { y: 15, autoAlpha: 0 })

    }
  }

}
</script>

<style scoped>
  i.title {
    font-size: 14px;
  }
  p {
    margin: 10px 0;
  }
  .readmore {
    font-size: 10px;
    font-weight: bold;
    color: var(--main-color);
    text-transform: uppercase;
  }
  h3 {
    text-shadow: 0.5px 0.5px 0px #454545;
  }

</style>

