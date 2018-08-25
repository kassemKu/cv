<template>
  <section class="container uk-height-viewport uk-padding-large">
    <h3 class="secondary-color">our skills</h3>

    <div class="uk-grid-collapse uk-child-width-1-3 uk-height-small" uk-grid>

      <HtmlSkill />

      <div class="uk-flex uk-flex-middle uk-flex-center">
        <div>
          1
        </div>
      </div>
      <!-- Column 2 -->

      <div class="uk-flex uk-flex-middle uk-flex-center">
        <div>
          1
        </div>
      </div>
      <!-- Column 3 -->



    </div>
    <!-- Grid -->

    </div>
  </section>
</template>

<script>
import HtmlSkill from '~/components/Skills/HtmlSkill';

export default {
  components: {
    HtmlSkill
  }
}
</script>
