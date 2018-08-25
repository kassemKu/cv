<template>
  <div class="uk-flex uk-flex-middle uk-flex-center">
    <div class="skill uk-position-relative">
      <div class="content uk-position-absolute">
        <div class="piece uk-position-absolute">
          <div class="outline"></div>
          <div class="fill"></div>
          <div class="num"></div>
        </div>
        
        <!-- <div class="piece uk-position-absolute">
          <div class="outline"></div>
          <div class="fill"></div>
          <div class="num"></div>
        </div>

        <div class="piece uk-position-absolute">
          <div class="outline"></div>
          <div class="fill"></div>
          <div class="num"></div>
        </div>

        <div class="piece uk-position-absolute">
          <div class="outline"></div>
          <div class="fill"></div>
          <div class="num"></div>
        </div>

        <div class="piece uk-position-absolute">
          <div class="outline"></div>
          <div class="fill"></div>
          <div class="num"></div>
        </div>

        <div class="piece uk-position-absolute">
          <div class="outline"></div>
          <div class="fill"></div>
          <div class="num"></div>
        </div>

        <div class="piece uk-position-absolute">
          <div class="outline"></div>
          <div class="fill"></div>
          <div class="num"></div>
        </div>

        <div class="piece uk-position-absolute">
          <div class="outline"></div>
          <div class="fill"></div>
          <div class="num"></div>
        </div>

        <div class="piece uk-position-absolute">
          <div class="outline"></div>
          <div class="fill"></div>
          <div class="num"></div>
        </div>

        <div class="piece uk-position-absolute">
          <div class="outline"></div>
          <div class="fill"></div>
          <div class="num"></div>
        </div>

        <div class="piece uk-position-absolute">
          <div class="outline"></div>
          <div class="fill"></div>
          <div class="num"></div>
        </div>

        <div class="piece uk-position-absolute">
          <div class="outline"></div>
          <div class="fill"></div>
          <div class="num"></div>
        </div>

        <div class="piece uk-position-absolute">
          <div class="outline"></div>
          <div class="fill"></div>
          <div class="num"></div>
        </div>

        <div class="piece uk-position-absolute">
          <div class="outline"></div>
          <div class="fill"></div>
          <div class="num"></div>
        </div>

        <div class="piece uk-position-absolute">
          <div class="outline"></div>
          <div class="fill"></div>
          <div class="num"></div>
        </div>

        <div class="piece uk-position-absolute">
          <div class="outline"></div>
          <div class="fill"></div>
          <div class="num"></div>
        </div>

        <div class="piece uk-position-absolute">
          <div class="outline"></div>
          <div class="fill"></div>
          <div class="num"></div>
        </div> -->

      </div>
    </div>
    <!-- skill -->
    
  </div>
  <!-- Column 1 -->
</template>

<script>
export default {
  name: 'html-skill',

  mounted() {
    this.$nextTick(this.movePieces);
  },

  methods: {
    movePieces() {
      let pieces = document.querySelectorAll('.piece');
      pieces.forEach(piece => {
        const tm = this.$gsap.TweenMax;
        const ease = this.$gsap.Linear.easeNone;

        tm.to(piece, .3, { y: 10, x: 10, ease: ease });
      })
    }
  }
}
</script>


<style scoped>
  /* Skills */
  .skill {
    width: 120px;
    height: 120px;
  }
  .content {
    width: 100%;
    height: 100%;
  }
  .piece {
    width: 20%;
    height: 20%;
  }
  .outline {
    width: 100%;
    height: 100%;
    background: url('/img/piece-outline-white.svg');
  }
  .outline::after {
    content: '';
    width: 100%;
    height: 100%;
    opacity: 0;
    top: 0;
    left: 0;
    position: absolute;
    background: url('/img/piece-fill-white.svg');
  }

  .piece:first-child, .fill:first-child {
    transform: rotate(21.18deg);
    margin-left: -5%;
    margin-top: -6%;
  }
  .piece:nth-child(2) {
    transform: rotate(42.36deg);
    margin-left: 6%;
    margin-top: 2%;
  }
  .piece:nth-child(3) {
    transform: rotate(63.54deg);
    margin-left: 14%;
    margin-top: 13%;
  }
  .piece:nth-child(4) {
    transform: rotate(84.72deg);
    margin-left: 18%;
    margin-top: 26%;
  }
  .piece:nth-child(5) {
    transform: rotate(105.9deg);
    margin-left: 17%;
    margin-top: 40%;
  }
  .piece:nth-child(6) {
    transform: rotate(.353turn);
    margin-left: 11%;
    margin-top: 54%;
  }
  .piece:nth-child(7) {
    transform: rotate(148.26deg);
    margin-left: 0%;
    margin-top: 64%;
  }
  .piece:nth-child(8) {
    transform: rotate(169.44deg);
    margin-left: -13%;
    margin-top: 69%;
  }
  .piece:nth-child(9) {
    transform: rotate(190.62deg);
    margin-left: -28%;
    margin-top: 69%;
  }
  .piece:nth-child(10) {
    transform: rotate(211.8deg);
    margin-left: -42%;
    margin-top: 64%;
  }
  .piece:nth-child(11) {
    transform: rotate(232.98deg);
    margin-left: -51%;
    margin-top: 54%;
  }
  .piece:nth-child(12) {
    transform: rotate(.706turn);
    margin-left: -57%;
    margin-top: 41%;
  }
  .piece:nth-child(13) {
    transform: rotate(275.34deg);
    margin-left: -58%;
    margin-top: 27%;
  }
  .piece:nth-child(14) {
    transform: rotate(296.52deg);
    margin-left: -54%;
    margin-top: 13%;
  }
  .piece:nth-child(15) {
    transform: rotate(317.7deg);
    margin-left: -45%;
    margin-top: 1%;
  }
  .piece:nth-child(16) {
    transform: rotate(338.88deg);
    margin-left: -33%;
    margin-top: -6%;
  }
  .piece:nth-child(17) {
    transform: rotate(360.06deg);
    margin-left: -19%;
    margin-top: -9%;
  }

</style>
