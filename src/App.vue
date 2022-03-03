<template>
  <router-view/>
</template>


<script>
// import GuideChimp from 'guidechimp';
// import 'guidechimp/dist/guidechimp.min.css';

export default {
  mounted() {
    // window.addEventListener('load', () => {
    //   // this.getActionFromURL();
    //   this.startGuidechimp()
    // })

    const script = document.createElement('script');
    script.setAttribute('src', 'https://hey-user-embed.netlify.app/js/app.js');
    script.setAttribute('type', 'text/javascript');
    document.getElementsByTagName('head')[0].appendChild(script);
    // Add a tag
    const wrapper = document.createElement("hey-user");
    wrapper.setAttribute('id', '1C51D7E6EF2B4148B6ABC7AF0019A99C');
    document.body.appendChild(wrapper);
  },

  methods:{
  }

}
</script>

<style lang="scss">
@import '~@/sass/main.scss';
#app {
  font-family: 'Source Sans Pro', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

body {
  margin: 0;
  background: var(--va-background);
}


/* Based on https://github.com/usablica/intro.js/issues/109#issuecomment-598328364 */

.introjs-helperLayer {
  background: transparent;
}

.introjs-overlay {
  opacity: 0 !important;
  z-index: 99999999!important;
}

.introjs-helperLayer:before {
  opacity: 0;
  content: '';
  position: absolute;
  width: inherit;
  height: inherit;
  border-radius: 0.5em;
  border: .2em solid rgba(255, 217, 68, 0.8);
  box-shadow: 0 0 0 1000em rgba(0,0,0, .7);
  opacity: 1;
}

.introjs-helperLayer:after {
  content: '';
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  position: absolute;
  z-index: 1000;
}



</style>
