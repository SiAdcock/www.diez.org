<template>
  <div>
    <div class="page shared">
      <NavBar></NavBar>
      <section class="hero">
        <div class="background"></div>
        <div class="section-split hero-container">
          <div class="half animation-holster">
            <div class="render-solve">Animation showing Diez in action</div>
            <HeroAnimation sizing="cover" loop="true"></HeroAnimation>
          </div>
          <div class="half align-top punch">
            <h1>The Design Language Framework</h1>
            <h3>Diez radically reduces the cost of delivering a consistent visual identity across your company’s apps &amp; websites.</h3>
            <router-link class="button left" to="/getting-started">Get Started</router-link>
            <a class="button secondary left" href="#enterprise-grade">Enterprise Edition</a>
          </div>
        </div>
      </section>

      <section id="what" class="section section-narrow">
        <h1 class="center heading1">What is Diez?</h1>
        <h3 class="center">Diez is a free &amp; open-source developer toolkit for expressing visual styles that can be shared across codebases, native platforms, and teams.
          <br><br>
          <strong>Diez comes in three parts:</strong>
        </h3>
      </section>

      <section id="dlf" class="section-split">
        <div  class="half align-top">
          <h2>1. Design language framework</h2>
          <p>Use TypeScript to compose <a href="/glossary/#tokens">design tokens</a> into <strong>scalable</strong> and <strong>extensible</strong> collections of styles, themes, and visual guidelines.  Your brand identity fits right here — as code.</p>
          <p>From colors to typography, drop shadows to border radii, gradients to usage guidelines, logos to icons: if you can imagine it, you can express it in Diez.</p>
        </div>
        <div class="half">
          <img width="100%" src="@theme/assets/imgs/dlf.png" alt="diez compiler">
        </div>
      </section>

      <section id="compiler" class="section-split">
        <div class="half mobile-reorder">
          <div class="video-holster alt card card-bordered">
            <video width="100%" autoplay loop muted playsinline>
              <source src="@theme/assets/vids/auto-complete.mp4" type="video/mp4">
            </video>
          </div>
        </div>
        <div class="half align-top">
          <h2>2. Cross-platform native compiler</h2>
          <p>Build any Diez project into pure native libraries for iOS, Android, or Web, ready for any new or existing codebase.</p>
          <p>Optimized for native-developer ergonomics — with autocomplete, inline documentation, and package manager support for iOS, Android, and Web: Diez makes it easy for everyone to rally around a common design language.</p>
        </div>
      </section>

      <section id="extractors" class="section-split">
        <div class="half align-top">
          <h2>3. Design file extractors</h2>
          <p>Diez Extractors compile design files into Diez-ready TypeScript — pulling colors, typography, image assets and more right out of your favorite design tools.</p>
          <p>Automate your design-to-development workflow by treating design files as versionable code artifacts.</p>
        </div>
        <div class="half mobile-reorder align-top">
          <div>
            <img width="100%" class="extractor-img" src="@theme/assets/imgs/extractors.jpg" alt="Design File Extractors: Sketch, Figma, InVision DSM">
          </div>
        </div>
      </section>

      <section id="enterprise-grade">
        <div class="section section-narrow no-bottom">
          <h1 class="center">Built for Enterprise</h1>
          <h3 class="center">Your design system’s missing half</h3>
          <p class="center">Diez naturally integrates with any UI component solution in the world to help you create a <strong>complete design system.</strong></p>
        </div>
        <div class="section full-img">
          <img src="@theme/assets/imgs/design-system.png" alt="design system" class="hide-on-mobile">
          <img src="@theme/assets/imgs/design-system-mobile.png" alt="design system" class="show-on-mobile mobile-img-spacer">
        </div>

        <div class="section-split">
          <div class="half align-top">
            <h2>Scales like a dream</h2>
            <p>Import, reuse & reference: great for composing multiple brands with shared assets & styles.</p>
            <p>Strongly typed from end-to-end, Diez scales to thousands of files, hundreds of codebases, and dozens of teams without skipping a beat.</p>
            <h3>Infinitely customizable</h3>
            <p>Diez is built around plugins: from the platforms it supports to the kinds of data you can express.  No matter the requirements of your design system — whether you’re wrangling one brand or a hundred — you can customize Diez to fit your needs.</p>
          </div>
          <div class="half" v-if="carouselComponent && slideComponent">
            <component :is="carouselComponent" :per-page="1" :loop="true" :autoplay="true" :speed="1000" :autoplayTimeout="3900" :paginationEnabled="false">
              <component :is="slideComponent" class="flex-centerer">
                <img width="55%" src="@theme/assets/imgs/simple.png" alt="simple" class="mobile-img-spacer center">
              </component>
              <component :is="slideComponent">
                <img width="90%" src="@theme/assets/imgs/complexity.png" alt="complexity" class="mobile-img-spacer">
              </component>
            </component>
          </div>
        </div>
      </section>

      <section id="docsgen" class="section-split">
        <div class="two-thirds mobile-reorder">
          <div class="video-holster card card-bordered">
            <video width="103%" style="margin-top:-6px;" autoplay loop muted playsinline preload="auto">
              <source src="@theme/assets/vids/docs.mp4" type="video/mp4">
            </video>
          </div>
        </div>
        <div class="one-third align-top">
          <h2>DocsGen Add-on</h2>
          <h3>(Enterprise Edition only)</h3>
          <p style="text-align: left;">From any Diez project, Diez DocsGen builds up-to-the-moment, customizable, and self-hostable design language docs as static HTML pages. <br><br> It's never been easier to get everyone in your organization speaking the same design language.</p>
        </div>
      </section>

      <section id="enterprise-cta" class="section-split">
        <div class="center">
          <h2>Learn more about Enterprise Edition</h2>
          <a class="button" :href="typeformUrl">
            Get in Touch
          </a>
        </div>
      </section>
    </div>

    <div id="enterprise" class="shared">
      <section class="section">
        <h1>Community & Enterprise Editions</h1>
        <p>Diez is available in two editions:  the free and open source <strong>Diez Community Edition</strong> with everything you need to create your design language source of truth — and <strong>Diez Enterprise Edition</strong> with exclusive access to DocsGen, customizable commercial licensing, and other enterprise value-adds.</p>
        <div class="side-by-side">
          <div class="card">
            <h3>Community Edition</h3>
            <ul>
              <li>Design language framework</li>
              <li>Diez Compiler</li>
              <li>Design file extractors</li>
              <li>Open source license</li>
            </ul>
            <router-link class="button secondary" to="/getting-started">Get Started</router-link>
          </div>
          <div class="card card-w-background card-bordered">
            <h3>Enterprise Edition</h3>
            <ul>
              <li>Design language framework</li>
              <li>Diez Compiler</li>
              <li>Design file extractors <span class="primary">(Including support for InVision DSM)</span></li>
              <li class="primary">DocsGen Add-on</li>
              <li class="primary">Commercial license</li>
              <li class="primary">Support, Integration, & Training</li>
            </ul>
            <a class="button" :href="typeformUrl">
              Get in Touch
            </a>
            <div class="background"></div>
          </div>
        </div>
      </section>
    </div>
    <Footer></Footer>
  </div>
</template>

<script>
import {sendGitHubClickEvent} from '../utils/analytics';
import Footer from '@theme/components/Footer.vue';
import NavBar from '@theme/components/NavBar.vue';

export default {
  data () {
    return {
      typeformUrl: 'https://design-code.typeform.com/to/JnOi9o',
      carouselComponent: null,
      slideComponent: null
    };
  },
  async mounted () {
    if (typeof window !== 'undefined') {
      const {Carousel, Slide} = await import('vue-carousel');
      this.carouselComponent = Carousel;
      this.slideComponent = Slide;

      const interval = setInterval(() => {
        if (window.currentBranch) {
          this.$data.typeformUrl = `${this.$data.typeformUrl}?sitevariant=${window.currentBranch}`;
          clearInterval(interval);
        }
      });
    }
  },
  methods: {
    sendGitHubClickEvent
  },
  components: {
    Footer,
    NavBar,
    HeroAnimation: () => import('@haiku/tina-diezheroinstancesyntax/vue')
  }
};
</script>

<style lang="scss" scoped>
  @import '@theme/styles/_utils.scss';

  .hero {
    position: relative;
    width: 100vw;
    margin: 0 auto;
    max-width: 2080px;
    height: 86vh;
    min-height: 400px;
    max-height: 800px;
    overflow: hidden;
    overflow-x: hidden !important;
    perspective: 1200px;
    border-bottom: 1px solid $palette-gray400;
    border-right: 1px solid $palette-gray400;
    border-left: 1px solid $palette-gray400;
    @include phone {
      height: auto;
      max-height: auto;
      margin-bottom: $spacing-xxxl-px;
      padding-bottom: $spacing-xxl-px;
    }
    h1 {
      font-size: 2.8rem;
      margin-top: 0;
      margin-bottom: 0;
    }
    .hero-container {
      display: flex;
      width: 100%;
      height: 100%;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      margin: $spacing-xxxl-px auto 0;

      h3 {
        font-size: 28px;
      }
    }
    .background {
      background-image: url("../assets/imgs/tileable@2x.png");
      width: 230%;
      height: 230%;
      position: absolute;
      left: 0;
      right: 0;
      opacity: .09;
      pointer-events: none;
      transform: rotateY(9deg) rotateX(20deg) rotateZ(-33deg) scale(.9) translateY(-67%) translateX(-30%);
      @include phone {
        transform: rotateY(9deg) rotateX(20deg) rotateZ(-33deg) scale(.9) translateY(-30%) translateX(0);
      }
    }
  }

  h1 {
    margin-bottom: $spacing-xxl-px;
  }

  h3 {
    margin-bottom: $spacing-lg-px;
  }

  li {
    font-weight: 700;
  }

  .heading1 {
    margin-top: $sizing-xs-px;
    @include phone {
      margin-top: $spacing-xl-px;
    }
  }

  .early-access h2 {
    color: $palette-primary;
  }

  .cta {
    @include typography-copy();
    background-color: $palette-purple;
    color: $palette-white;
    text-align: center;
    @include phone {
      flex-direction: column;
      a.button {
        margin-top: $spacing-lg-px !important;
      }
    }
  }

  .cta {
    margin-top: $spacing-xxxl-px;
    padding: $spacing-xxxl-px $spacing-xxxl-px $spacing-xxl-px;
  }

  .handle-it {
    $handle-height: 83px;
    margin: -$handle-height auto 0;
    display: block;
    width: 70px;
    z-index: -1;
    @include tablet {
      margin-top: $handle-height / 2;
    }
  }

  .output-it {
    display: block;
    margin: 0 auto;
    width: 210px;
    z-index: -1;
  }

  .card.half {
    position: relative;
    width: 35%;
    overflow: visible;
    margin: 0 auto;
    img {
      margin: 30px 30px 10px;
    }
    font-weight: 700;
    text-align: center;
    padding-bottom: 30px;
  }

  .img-outline {
    border: 1px solid $palette-gray400;
  }

  .cta-holster {
    margin-top: $spacing-xs-px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: $sizing-md-px;
  }

  .video-holster {
    position: relative;
    width: 100%;
    height: 0;
    padding-bottom: 56.25%;
    &.alt {
      padding-bottom: 62.25%;
    }
  }

  .video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }

  .bottom-spacer {
    margin-bottom: $sizing-xs-px;
  }

  .temp-img {
    transform: translate(-240px, 20px);
  }

  .animation-holster {
    min-width: 50%;
    min-height:100%;
    padding-left: 0;
    @include tablet-large {
      display: none;
    }
  }

  .punch {
    padding-left: 30px;
    @include tablet-large {
      width: 100%;
    }
    @include phone {
      text-align: center;
      padding: $spacing-lg-px;

      .button.left {
        float: none;
      }
    }
  }

  .render-solve {
    opacity: 0;
    pointer-events: none;
  }

  #enterprise-grade {
    margin-top: $spacing-xxxl-px;
  }

  #dlf {
    margin-top: -70px;
    @include phone {
      margin-top: -20px;
    }
  }

  #docsgen {
    h2 {
      margin-bottom: $spacing-lg-px;
    }
    h3 {
      margin-top: 0;
    }
  }

  #enterprise {
    font-family: "Source Sans Pro",sans-serif;
    font-size: 20px;
    background-color: $palette-mauve;
    h1 {
      text-align: center;
      color: $palette-white;
      margin-bottom: $spacing-lg-px;
    }
    h2 {
      color: $palette-white;
      margin-bottom: $spacing-xs-px;
    }
    h3 {
      margin-top: $spacing-xs-px;
    }
    p {
      text-align: center;
      max-width: $sizing-xxl-px;
      margin: 0 auto;
      margin-bottom: $spacing-xxl-px;
    }
    section {
      margin-bottom: 0;
      margin-top: $sizing-xs-px;
      padding-bottom: $sizing-xs-px;
    }
  }

  .side-by-side {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    .card {
      margin: 0 $spacing-lg-px;
      padding: $spacing-lg-px $spacing-xxxl-px $spacing-xl-px;
      text-align: center;
      max-width: 37%;
      @include phone {
        padding: $spacing-lg-px $spacing-lg-px $spacing-xl-px;
        max-width: 100%;
      }
      h3 {
        text-align: center;
        margin: $spacing-lg-px;
      }
      ul {
        text-align: left;
        margin-bottom: $spacing-xxl-px;
      }
      @include tablet {
        width: 100%;
      }
    }
  }

  .card-bordered {
    border: 1px solid $palette-card-color;
  }

  .card-w-background {
    perspective: 1200px;
    position: relative;
    overflow: hidden;
    background-color: $palette-white;
    .background {
      background-image: url("../assets/imgs/tileable@2x.png");
      width: 230%;
      height: 230%;
      position: absolute;
      left: 0;
      right: 0;
      opacity: .09;
      pointer-events: none;
      transform: rotateY(9deg) rotateX(20deg) rotateZ(-33deg) scale(.9) translate(12%, -80%);
      @include phone {
        transform: rotateY(9deg) rotateX(20deg) rotateZ(-33deg) scale(.9) translate(55%, -80%);
      }
    }
    .primary {
      color: $palette-primary;
    }
    @include tablet {
      margin-top: $spacing-lg-px !important;
    }
  }

  .code-block {
    width: 100%;
  }

  #what {
    margin-bottom: 0;
  }

  .full-img {
    text-align: center;
    padding-top: 0;
    @include phone {
      margin-bottom: $spacing-xxxl-px;
    }

    img {
      width: 67%;
      @include tablet {
        width: 100%;
      }
      @include phone {
        width: 90%;
      }
    }
  }

  .mobile-img-spacer {
    @include tablet {
      padding-top: $spacing-lg-px;
    }
  }

  .section-split {
    margin-bottom: $spacing-lg-px;
  }

  @include phone {
    .shared.page {
      padding-top: $spacing-xl-px;
    }

    h3 {
      padding-left: 0;
      padding-right: 0;
    }
  }

  .extractor-img {
    margin-top: 25px;
    @include phone {
      margin-top: 0;
    }
  }

  .flex-centerer {
    display: flex;
    align-items: center;
    justify-content: center;
  }

</style>
