<template>
  <div class="uk-position-top-right uk-position-fixed uk-margin-small-top uk-margin-right">
    <ul class="uk-subnav" uk-margin>
      <li>
        <nuxt-link to="/" class="link-btn link-btn-home uk-position-relative">
          home
        </nuxt-link>
      </li>
      <li>
        <nuxt-link :to="{ name: 'about' }" class="link-btn uk-position-relative uk-padding-small">
          about
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/skills" class="link-btn uk-position-relative">
          skills
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/works" class="link-btn uk-position-relative">
          my works
        </nuxt-link>
      </li>
    </ul>
  </div>
  <!-- Top Nav -->
</template>

<script>

export default {
  
}
</script>

<style scoped>
/* ** navLink && Nav Link Hover ** */
.uk-subnav > li > a {
   font-size: 10px;
   font-weight: bold;
   color: #cccccc;
}
  a.link-btn {
    overflow: hidden;
    padding: 4px 5px;
    -webkit-transition: all 300ms linear;
    transition:         all 300ms linear;
    box-shadow: 0px 0px 1px 1px rgba(255,255,255, 0.1);
  }
  a.link-btn:hover, .nuxt-link-exact-active {
    color: #816f19 !important;
    background: transparent;
  }
  a.link-btn::before, a.link-btn::after {
    content: '';
    position: absolute;
    display: block;
    width: 100%;
    height: 2px;
    background: #816f19;
    box-sizing: border-box;
   -webkit-transition: all 350ms cubic-bezier(0.95, 0.05, 0.795, 0.035);
    transition:         all 350ms cubic-bezier(0.95, 0.05, 0.795, 0.035);
  }
  a.link-btn::before {
    top: 0;
    left: 100%;
  }
  a.link-btn:hover::before {
   left: 0;
  }
  a.link-btn::after {
    bottom: 0;
    right: 100%;
  }
  a.link-btn:hover::after {
    right: 0;
  }
</style>


