<template>
  <div class="main-container uk-height-viewport uk-flex uk-flex-center uk-text-center">
    <div class="content">
      <h1>I am ahmad kassem <span class="secondary-color">koulaib</span></h1>
      <p>
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Exercitationem, veniam?
      </p>
      <div class="uk-container uk-padding">
        <div class="uk-child-width-1-2@s" uk-grid>
          <div>
            <blockquote cite="#" class="uk-column-span uk-text-small">
              <p>All we have to decide is what to do with the time that is given us.</p>
              <footer class="uk-text-small">Gandalf in in <cite><a href="#">The Fellowship of the Ring</a></cite></footer>
            </blockquote>
          </div>
          <div>
            <blockquote cite="#" class="uk-column-span uk-text-small">
              <p>All we have to decide is what to do with the time that is given us.</p>
              <footer class="uk-text-small">Gandalf in in <cite><a href="#">The Fellowship of the Ring</a></cite></footer>
            </blockquote>
          </div>
        </div>
      </div>
      <div class="uk-flex uk-flex-center uk-margin">
        <ul class="uk-subnav" uk-margin>
          <li>
            <a href="#" class="sequare-border uk-button uk-button-default uk-box-shadow-small">
              <span uk-icon="icon: cloud-download"></span>
              download CV
            </a>
          </li>
          <li>
            <a href="#" class="sequare-border uk-button uk-button-default uk-box-shadow-small">
              meet me
            </a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'page-index',
  }
</script>

<style scoped>
  .content {
    margin-top: 20vh;
  }
  .content h1 {
    text-shadow: 1px 0px 0px #454545;
  }
   .content h1, span {
    opacity: .8;
  }
</style>
