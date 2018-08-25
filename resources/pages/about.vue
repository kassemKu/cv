<template>
  <section class="container uk-height-viewport">
    <div class="uk-grid-small uk-padding-large" uk-grid>
      <div class="uk-width-1-3@s">
        <img src="/img/personal.png" width="300" height="450" alt="ahamd kassem koulaib" class="uk-border-rounded">
        <div class="uk-text-center">
          <i class="uk-article-meta">i am ahamd kassem koulaib</i>
        </div>
        
        <ul class="uk-list">
          <li>
            <span class="uk-margin-right">
              <img src="~/assets/img/icons/mail2.svg" alt="ahamd" width="16" height="16" uk-svg>
            </span>
            <i>
              <a class="uk-link-reset" href="">arabisc95@gmail.com</a>
            </i>
          </li>
          <li>
            <span class="uk-margin-right">
              <img src="~/assets/img/icons/chrome.svg" alt="ahamd" width="16" height="16" uk-svg>
            </span>
            <i>
              <a class="uk-link-reset" href="#">https://arabisc.com</a>
            </i>
          </li>
          <li>
            <span class="uk-margin-right">
              <img src="~/assets/img/icons/point-right.svg" alt="ahamd" width="16" height="16" uk-svg>
            </span>
            <i>triboli-south-libnaon-moharam</i>
          </li>
          <li>
            <span class="uk-margin-right">
              <img src="~/assets/img/icons/phone.svg" alt="ahamd" width="16" height="16" uk-svg>
            </span>
            <i>00961-76-114-669</i>
          </li>
        </ul>
      </div>
      <div class="uk-width-2-3@s uk-padding uk-flex uk-flex-middle">
        <div class="">
          <p>
            <i class="text uk-text-strong">
              I am Ahmad Klaib, I born in <b class="secondary-color">Talkalakh</b>  Town in 1984, <abbr title="text">I left Syria in 2012 to Lebanon</abbr> , I started learning coding there,
              <br>
              I fall in love coding and web languages especially, I am spending almost of the time in acquiring new software skills.
            </i>
          </p>
          <p>
            <i class="text uk-text-strong">
              <q>I am hard worker</q>, I work 14 hours a day, I have built many web sites in different coding languages,I have more than five years of experience in web design and programming, I can work on almost web develop languages but I am  perfect in <span class="secondary-color">Java script, php, python</span>, and its liberaries
              <br>
              <b>Coding became my passion,</b> I follow a day by day to learn any new skill in programming   
            </i>
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
  export default {
    name: 'page-about',

    head () {
      return {
        
      }
    },
  }
</script>

<style>
  li > * {
    font-size: 10px;
    font-weight: bold;
    color: var(--main-color);
    text-transform: uppercase;
  }
  strong {
    color: var(--main-color);
    text-transform: uppercase;
  }
  i.text {
    font-size: 13px;
  }
</style>

