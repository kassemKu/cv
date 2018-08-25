<template>
  <div class="default uk-container-expand">
    <div class="bg-canvas uk-position-absolute uk-height-viewport uk-width-1-1">
    </div>
   <!-- Overlay Canvs -->
   
    <div class="mouse-icon-circle" id="mouse-icon-circle"
    :style="{ width: icon.width, height: icon.height }"
    v-model="icon">
      <div>
        <span class="mouse-icon-square" id="mouse-icon-square"></span>
      </div>
    </div>
   <!-- Follow Mouse -->
    <TopNav />
    <SocialNav />
    <TitlePart />
    <CopyRight />

    <!-- <span class="follow-mouse uk-position-center uk-position-absolute" id="ball">
      <span class="pencil uk-position-absolute" uk-icon="icon: pencil; ratio: 1.2"></span>
    </span> -->
    <!-- Follow Mouse -->

    <div class="uk-container uk-z-index">
      <nuxt/>
    </div>
    <!-- Content -->
  </div>
</template>

<script>
  // const MyFooter = () => import('~/components/MyFooter')
  const TopNav = () => import('~/components/Navs/TopNav.vue');
  const SocialNav = () => import('~/components/Navs/SocialNav.vue');
  const TitlePart = () => import('~/components/Navs/TitlePart.vue');
  const CopyRight = () => import('~/components/Navs/CopyRight.vue');

  export default {
    name: 'layout-default',

    components: {
      TopNav,
      SocialNav,
      TitlePart,
      CopyRight
    },

    data() {
      return {
        mouse: {
           x: 0,
           y: 0
        },
        icon: {
           x: 0,
           y: 0,
           left: 0,
           top: 0,
        },
      };
      
    },

    mounted() {
      this.$nextTick(this.followMouse);
    },

    methods: {

      followMouse() {

        const $ = document.querySelector.bind(document);
        const $on = document.addEventListener.bind(document);
        
        var mouseIconSquare = $('#mouse-icon-square');
        var mouseIconCircle = $('#mouse-icon-circle');

        var mouseData = this.$data.mouse;
        var iconData = this.$data.icon;

        const tm = this.$gsap.TweenMax;
        const ease = this.$gsap.Linear.easeNone;

        let mouseIsMove = false;

        $on('mousemove', mouseMoved);
        function mouseMoved (e) {
          mouseData.x = e.clientX || e.pageX;
          mouseData.y = e.clientY || e.pageY;
          if (!iconData.x || !iconData.y || mouseIsMove) {
            iconData.x = mouseData.x;
            iconData.y = mouseData.y;
          };
          tm.to(mouseIconCircle, .3, { x: iconData.x, y: iconData.y, ease: ease });
          mouseIsMove = true;
        }


        // Create a new Timeline (equivalent to new TimelineMax())
        // const tl = new this.$gsap.TimelineMax()

        // tl
        //   .to(mouseIconCircle, 1, { x: 200, y: 200, ease: this.$gsap.Linear.easeNone })
          // .to(mouseIconSquare, 1, { x: 5, y: 5, ease: this.$gsap.Linear.easeNone });

      //   var $ = document.querySelector.bind(document);
      //   var $on = document.addEventListener.bind(document);

      //   var mouseX, mouseY;
      //   $on('mousemove', function (e) {
      //     mouseX = e.clientX || e.pageX;
      //     mouseY = e.clientY || e.pageY;
          
      //     var ball = $('#ball');
          
      //     var x = void 0, y = void 0, dx = void 0, dy = void 0, tx = 0, ty = 0, key = -1;

      //       // key = requestAnimationFrame(followMouse);

      //       if(!x || !y) {
      //         x = mouseX;
      //         y = mouseY;
      //       }else {
      //         dx = (mouseX - x) * 0.125;
      //         dy = (mouseY - y) * 0.125;

      //         if(Math.abs(dx) + Math.abs(dy) < 0.1) {
      //           x = mouseX;
      //           y = mouseY;
      //         }else {
      //           x += dx;
      //           y += dy;
      //         }
      //       }

      //       ball.style.left = x + 'px';
      //       ball.style.top = y + 'px';
      //       ball.style.visibility = "visible";

      //   });
      },
    },

  };
</script>

<style scoped>
/* ** Background Overlay Canvas ** */
.bg-canvas {
  /* background: url('/img/bg_canvas-repeat_grey.jpg') repeat 50%/400px 200px; */
  background: url('/img/dark-noise-background.jpg') center center;
  background-size: cover;
  z-index: -1;
}
/* .bg-canvas::after {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%; */
  /* background: url('/img/_texture.png') repeat 50%/130px 130px; */
  /* background: url('/img/noise.jpg');
} */


.mouse-icon-circle {
  /* width: 20px;
  height: 20px; */
  position: absolute;
  z-index: 1;
  background: transparent;
  /* margin: 40px; */
  width: 20px;
  height: 20px;
  border: 2px solid #816f19;
  border-radius: 50%;
  box-shadow: 0px 0px 2px 2px rgba(255,255,255, 0.2);
}
.mouse-icon-square {
  position: absolute;
  display: block;
  top: 50%;
  left: 50%;
  width: 3px;
  height: 3px;
  transform: translate(-50%, -50%);
  display: block;
  background: #999999;
  box-shadow: 0px 0px 1px 1px rgba(255,255,255, 0.3);
}

</style>
