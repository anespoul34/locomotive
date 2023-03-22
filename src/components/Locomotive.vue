<script>
import locomotiveScroll from "locomotive-scroll";
export default {
  name: "locoScroll",
  data() {
    return {
      scrollIns: null
    };
  },
  mounted() {
    const _self = this;
    this.$nextTick(function() {
      _self.initLocoScroll();
    });
  },
  methods: {
    initLocoScroll() {
      const _self = this;
      this.scroll = new locomotiveScroll({
        el: _self.$refs['scrollSections'],
        smooth: true,
        getDirection: true
      });
    }
  }
};
</script>

<template>
  <div ref="scrollSections">
    <div id="header">
      <a href="mailto:nespoulous.arthur@yahoo.fr" class="contact-button">
          <span class="underline-animation">Contact</span>
      </a>
  </div>
  <div id="home-page" class="main-container">
      <section id="page0" class="page page--0 fcolcc" data-scroll-section>
          <div class="wrapper fcolcfs">
              <div class="container" data-scroll data-scroll-speed="-12" data-scroll-target="#page0">
                  <h1>Arthur</h1>
                  <h1>Nespoulous</h1>
                  <div class="line"></div>
                  <h2>Freelance</h2>
                  <h2>Front-End Developer</h2>
              </div>
              <div class="design-block" data-scroll data-scroll-direction="vertical" data-scroll-speed="1" data-scroll-target="#page0">
                  <div class="dsgn" data-scroll data-scroll-direction="horizontal" data-scroll-speed="30" data-scroll-target="#page0"></div>
              </div>
              <div class="scroll-icon" data-scroll data-scroll-speed="-6" data-scroll-target="#page0">
                  <div id="arrow-wrapper">
                      <div id="arrow-wrapper-inner">
                      <div id="scroll-down">
                          <span class="arrow-down">
                          </span>
                      </div>
                      </div>
                  </div>
                  <span>Scroll</span>
                  <span>Down</span>
              </div>
          </div>
      </section>
      <section id="page1" class="page page--1 fcolfsc" data-scroll-section>
          <div class="page1-container" data-scroll data-scroll-sticky data-scroll-target="#page1">
              <div class="scrollable__banner">
                  <div class="scrollable__banner--inner scrollable__banner--2 ffec" 
                      data-scroll
                      data-scroll-target="#page1"
                      data-scroll-direction="horizontal"
                      data-scroll-speed="-22">
                      <span>C/C#</span>
                      <span>JavaScript</span>
                      <span>TypeScript</span>
                      <span>HTML</span>
                      <span>SCSS</span>
                      <span>Node</span>
                  </div>
              </div>
              <div class="scrollable__banner">
                  <div class="scrollable__banner--inner scrollable__banner--1 ffsc" 
                      data-scroll 
                      data-scroll-target="#page1"
                      data-scroll-direction="horizontal"
                      data-scroll-speed="20">
                      <span>Angular</span>
                      <span>React</span>
                      <span>Unity</span>
                      <span>ThreeJs</span>
                      <span>MySQL</span>
                  </div>
              </div>
          </div>
          <div class="infos-container">
              <p>Hi, my name is <strong>Arthur</strong>, graduated from <strong>Ecole 42</strong>.<br/>I'm a <strong>Front-End Developer</strong> from France for 4 years.</p>
              <p>Passionate about <strong>Web technologies</strong> and <strong>video games</strong>. I love working at the intersection of creativity and user friendly interfaces.</p>
          </div>
      </section>
      <section id="page2" class="page page--2 fcc" data-scroll-section>
          <div class="page-container fcolcfs">
              <span>Last Login:</span>
              <div class="line"></div>
              <div class="main-content fcc">
                  <p>&lt;p&gt;When I’m not working on new websites, I’m probably <span>playing</span> games or <span>building</span> them.&lt;p/&gt;</p>
              </div>
              <div class="line"></div>
              <span>FR (46°16’10.56’’N, 5°31’44.888”E)</span>
          </div>
      </section>
      <section id="page3" class="page page--3 fcolcc" data-scroll-section>
          <div class="main fcc">
              <a href="mailto:nespoulous.arthur@yahoo.fr" class="container fcolcfs">
                  <div class="fcc">
                      <p>Available</p>
                      <div class="emote"><span>👋</span></div>
                  </div>
                  <p>for project</p>
              </a>
          </div>
          <div class="footer fsbc">
              <div class="fcolcfs">
                  <span class="name">Arthur Nespoulous</span>
                  <span class="job">Freelance Front-End Developer</span>
              </div>
              <div class="fcc">
                  <a href="https://www.linkedin.com/in/arthur-nespoulous-956970142" target="_blank">
                      <img src="@/assets/images/linkedin.png" alt="linkedin link">
                  </a>
                  <a href="https://github.com/anespoul34" target="_blank">
                      <img src="@/assets/images/github.png" alt="github link">
                  </a>
                  <a href="https://www.malt.fr/profile/arthurnespoulous" target="_blank">
                      <img src="@/assets/images/malt.png" alt="malt link">
                  </a>
              </div>
          </div>
      </section>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import '@/assets/merle-scss/main.scss';

h1, h2, p, span {
    cursor: default;
}
a {
    span, p {
        cursor: pointer;
    }
}

#header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 94px;
    display: flex;
    justify-content: flex-end;
    align-items: flex-end;
    z-index: 99;
    padding: 0 200px 0 180px;
    mix-blend-mode: difference;

    a {
        span {
            font-size: 2rem;
            text-transform: uppercase;
            font-family: 'Space Grotesk', sans-serif;
        }
    }
}

section {
    scroll-snap-type: y mandatory;
}

.page {
    width: 100%;
    height: 100vh;
    overflow: hidden;

    &--0 {
        height: 100vh;
        background: red;
        position: relative;
        .wrapper {
            width: 100%;
            height: 100%;
            position: relative;
            background: #000;
            padding: 10rem 200px 0 180px;

            .container {
                width: 100%;
                z-index: 1;
                mix-blend-mode: difference;
                // background: #ffffe9;

                .line {
                    width: 100%;
                    height: 2px;
                    background: #fff;
                    margin: 44px 0;
                }
            }
            h1, h2 {
                z-index: 1;
                color: #fff;
                font-size: 18rem;
                font-family: 'Space Grotesk', sans-serif;
                margin: 0;
                font-weight: 500;
                text-transform: uppercase;
                line-height: 1;
            }
            h2 {
                font-size: 4rem;
                line-height: 1.4;
            }
            .design-block {
                position: absolute;
                bottom: 0;
                right: 0;
                width: 50rem;
                height: 50rem;

                .dsgn {
                    width: 100%;
                    height: 100%;
                    border-radius: 50%;
                    background: #ffffe9;
                }
            }
        }
        .scroll-icon {
            position: absolute;
            bottom: 20px;
            right: 200px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            mix-blend-mode: difference;

            span {
                text-transform: uppercase;
                color: #fff;
                font-size: 1.9rem;
                font-family: 'Space Grotesk', sans-serif;
            }
        }
    }
    &--1 {
        height: 350vh;
        background: #ffffe9;
        mix-blend-mode: difference;
        padding-top: 20rem;
        position: relative;

        .scrollable {
            position: absolute;
            width: 100%;
        
            &__banner {
                width: 100%;
                transform: rotate(-5deg);

                &--inner {
                    width: 100%;
        
                    span {
                        font-size: 18rem;
                        font-family: "Space Grotesk", sans-serif;
                        color: #000;
                        margin: 0 5rem;
                    }
                }
            }
        }
        .infos-container {
            position: absolute;
            bottom: 50vh;
            left: 50%;
            transform: translate(-50%, 50%);
            max-width: 69rem;
            background: #000;
            mix-blend-mode: difference;

            p {
                font-size: 3rem;
                font-family: "Space Grotesk", sans-serif;
                color: #ffffe9;;
            }
            strong {
                font-weight: bold;
            }
        }
    }
    &--2 {
        padding: 14.5rem 10%;
        background: #000;

        .page-container {
            width: 100%;
            height: 100%;
            max-width: 1220px;

            .line {
                margin: 15px 0 5px 2px;
                width: 16px;
                height: 5px;
                background: #fff;
                animation-name: blink;
                animation-duration: 0.4s;
                animation-direction: alternate;
                animation-iteration-count: infinite;
                animation-timing-function: ease-out;
            }
            span {
                color: #fff;
                font: {
                    family: "Space Grotesk", sans-serif;
                    size: 3.4rem;
                }
                text-transform: uppercase;
            }
            .main-content {
                flex: 1 0 auto;
                max-width: 120rem;
                p, span {
                    color: #fff;
                    font-size: 7.6rem;
                    text-transform: uppercase;
                    font-family: "Space Grotesk", sans-serif;
                    line-height: 1.1;
                }
                span {
                    position: relative;
                }
                span::after {
                    content: '';
                    position: absolute;
                    bottom: 10px;
                    left: 0;
                    height: 4px;
                    width: 100%;
                    background: #fff;
                    animation: 5s lineGrowth ease-in-out infinite;
                }
            }
        }
    }
    &--3 {
        .main {
            flex: 1 0 auto;
            background: #D9DDDF;
            width: 100%;
            
            p, span {
                font-family: "Space Grotesk", sans-serif;
                font-size: 16rem;
                color: #000;
                font-weight: bold;
                margin: 0;
                text-transform: uppercase;
                line-height: 1;
            }
            .emote {
                transform-origin: 75% 100%;
                animation: 0.5s handRotation alternate ease-in-out infinite;
            }
        }
        .footer {
            width: 100%;
            height: 130px;
            background: #000;
            padding: 0 24rem 0 12rem;

            .name {
                text-transform: uppercase;
                font-size: 2rem;
                color: #fff;
                font-family: "Space Grotesk", sans-serif;
                font-weight: bold;
            }
            .job {
                font-size: 2rem;
                color: #fff;
                font-family: "Space Grotesk", sans-serif;
            }

            img {
                max-height: 5.6rem;
                margin: 0 2rem;
            }
        }
    }
}

/*
============
Down Arrow
============
*/

#scroll-down:hover,
#scroll-down:focus{
    cursor: pointer;
}

#arrow-wrapper {
  display: table;
  width:100%;
  height:100%;
}

#arrow-wrapper-inner {
  display: table-cell;
  vertical-align:middle;
  width:100%;
  height:100%;
  text-align: center
}

#scroll-down {
    display: inline-block;
    position: relative;
    padding-top: 79px;
    text-align:center;
}
.arrow-down {
    display: block;
    margin: 0 auto;
    width: 14px;
    height: 25px;
}
.arrow-down:after {
    content: '';
    display: block;
    margin: 0;
    padding: 0;
    width: 12px;
    height: 12px;
    border-top: 2px solid #fff;
    border-right: 2px solid #fff;
    // behavior: url(-ms-transform.htc);
    -moz-transform: rotate(135deg);
    -webkit-transform: rotate(135deg);
    -o-transform: rotate(135deg);
    -ms-transform: rotate(135deg);
    transform: rotate(135deg);
}
#scroll-down::before {
    -webkit-animation: elasticus 1.2s cubic-bezier(1, 0, 0, 1) infinite;
    /* Safari 4+ */
    
    -moz-animation: elasticus 1.2s cubic-bezier(1, 0, 0, 1) infinite;
    /* Fx 5+ */
    
    -o-animation: elasticus 1.2s cubic-bezier(1, 0, 0, 1) infinite;
    /* Opera 12+ */
    
    animation: elasticus 1.2s cubic-bezier(1, 0, 0, 1) infinite;
    /* IE 10+, Fx 29+ */
    
    position: absolute;
    top: 53px;
    left: 50%;
    margin-left: -1px;
    width: 2px;
    height: 40px;
    background: #fff;
    content: ' ';
}
@-webkit-keyframes elasticus {
    0% {
        -webkit-transform-origin: 0% 0%;
        -ms-transform-origin: 0% 0%;
        -moz-transform-origin: 0% 0%;
        -o-transform-origin: 0% 0%;
        transform-origin: 0% 0%;
        -webkit-transform: scale(1, 0);
        -ms-transform: scale(1, 0);
        -moz-transform: scale(1, 0);
        -o-transform: scale(1, 0);
        transform: scale(1, 0);
    }
    50% {
        -webkit-transform-origin: 0% 0%;
        -ms-transform-origin: 0% 0%;
        -moz-transform-origin: 0% 0%;
        -o-transform-origin: 0% 0%;
        transform-origin: 0% 0%;
        -webkit-transform: scale(1, 1);
        -ms-transform: scale(1, 1);
        -moz-transform: scale(1, 1);
        -o-transform: scale(1, 1);
        transform: scale(1, 1);
    }
    50.1% {
        -webkit-transform-origin: 0% 100%;
        -ms-transform-origin: 0% 100%;
        -moz-transform-origin: 0% 100%;
        -o-transform-origin: 0% 100%;
        transform-origin: 0% 100%;
        -webkit-transform: scale(1, 1);
        -ms-transform: scale(1, 1);
        -moz-transform: scale(1, 1);
        -o-transform: scale(1, 1);
        transform: scale(1, 1);
    }
    100% {
        -webkit-transform-origin: 0% 100%;
        -ms-transform-origin: 0% 100%;
        -moz-transform-origin: 0% 100%;
        -o-transform-origin: 0% 100%;
        transform-origin: 0% 100%;
        -webkit-transform: scale(1, 0);
        -ms-transform: scale(1, 0);
        -moz-transform: scale(1, 0);
        -o-transform: scale(1, 0);
        transform: scale(1, 0);
    }
}
@-moz-keyframes elasticus {
    0% {
        -webkit-transform-origin: 0% 0%;
        -ms-transform-origin: 0% 0%;
        -moz-transform-origin: 0% 0%;
        -o-transform-origin: 0% 0%;
        transform-origin: 0% 0%;
        -webkit-transform: scale(1, 0);
        -ms-transform: scale(1, 0);
        -moz-transform: scale(1, 0);
        -o-transform: scale(1, 0);
        transform: scale(1, 0);
    }
    50% {
        -webkit-transform-origin: 0% 0%;
        -ms-transform-origin: 0% 0%;
        -moz-transform-origin: 0% 0%;
        -o-transform-origin: 0% 0%;
        transform-origin: 0% 0%;
        -webkit-transform: scale(1, 1);
        -ms-transform: scale(1, 1);
        -moz-transform: scale(1, 1);
        -o-transform: scale(1, 1);
        transform: scale(1, 1);
    }
    50.1% {
        -webkit-transform-origin: 0% 100%;
        -ms-transform-origin: 0% 100%;
        -moz-transform-origin: 0% 100%;
        -o-transform-origin: 0% 100%;
        transform-origin: 0% 100%;
        -webkit-transform: scale(1, 1);
        -ms-transform: scale(1, 1);
        -moz-transform: scale(1, 1);
        -o-transform: scale(1, 1);
        transform: scale(1, 1);
    }
    100% {
        -webkit-transform-origin: 0% 100%;
        -ms-transform-origin: 0% 100%;
        -moz-transform-origin: 0% 100%;
        -o-transform-origin: 0% 100%;
        transform-origin: 0% 100%;
        -webkit-transform: scale(1, 0);
        -ms-transform: scale(1, 0);
        -moz-transform: scale(1, 0);
        -o-transform: scale(1, 0);
        transform: scale(1, 0);
    }
}
@-o-keyframes elasticus {
    0% {
        -webkit-transform-origin: 0% 0%;
        -ms-transform-origin: 0% 0%;
        -moz-transform-origin: 0% 0%;
        -o-transform-origin: 0% 0%;
        transform-origin: 0% 0%;
        -webkit-transform: scale(1, 0);
        -ms-transform: scale(1, 0);
        -moz-transform: scale(1, 0);
        -o-transform: scale(1, 0);
        transform: scale(1, 0);
    }
    50% {
        -webkit-transform-origin: 0% 0%;
        -ms-transform-origin: 0% 0%;
        -moz-transform-origin: 0% 0%;
        -o-transform-origin: 0% 0%;
        transform-origin: 0% 0%;
        -webkit-transform: scale(1, 1);
        -ms-transform: scale(1, 1);
        -moz-transform: scale(1, 1);
        -o-transform: scale(1, 1);
        transform: scale(1, 1);
    }
    50.1% {
        -webkit-transform-origin: 0% 100%;
        -ms-transform-origin: 0% 100%;
        -moz-transform-origin: 0% 100%;
        -o-transform-origin: 0% 100%;
        transform-origin: 0% 100%;
        -webkit-transform: scale(1, 1);
        -ms-transform: scale(1, 1);
        -moz-transform: scale(1, 1);
        -o-transform: scale(1, 1);
        transform: scale(1, 1);
    }
    100% {
        -webkit-transform-origin: 0% 100%;
        -ms-transform-origin: 0% 100%;
        -moz-transform-origin: 0% 100%;
        -o-transform-origin: 0% 100%;
        transform-origin: 0% 100%;
        -webkit-transform: scale(1, 0);
        -ms-transform: scale(1, 0);
        -moz-transform: scale(1, 0);
        -o-transform: scale(1, 0);
        transform: scale(1, 0);
    }
}
@keyframes elasticus {
    0% {
        -webkit-transform-origin: 0% 0%;
        -ms-transform-origin: 0% 0%;
        -moz-transform-origin: 0% 0%;
        -o-transform-origin: 0% 0%;
        transform-origin: 0% 0%;
        -webkit-transform: scale(1, 0);
        -ms-transform: scale(1, 0);
        -moz-transform: scale(1, 0);
        -o-transform: scale(1, 0);
        transform: scale(1, 0);
    }
    50% {
        -webkit-transform-origin: 0% 0%;
        -ms-transform-origin: 0% 0%;
        -moz-transform-origin: 0% 0%;
        -o-transform-origin: 0% 0%;
        transform-origin: 0% 0%;
        -webkit-transform: scale(1, 1);
        -ms-transform: scale(1, 1);
        -moz-transform: scale(1, 1);
        -o-transform: scale(1, 1);
        transform: scale(1, 1);
    }
    50.1% {
        -webkit-transform-origin: 0% 100%;
        -ms-transform-origin: 0% 100%;
        -moz-transform-origin: 0% 100%;
        -o-transform-origin: 0% 100%;
        transform-origin: 0% 100%;
        -webkit-transform: scale(1, 1);
        -ms-transform: scale(1, 1);
        -moz-transform: scale(1, 1);
        -o-transform: scale(1, 1);
        transform: scale(1, 1);
    }
    100% {
        -webkit-transform-origin: 0% 100%;
        -ms-transform-origin: 0% 100%;
        -moz-transform-origin: 0% 100%;
        -o-transform-origin: 0% 100%;
        transform-origin: 0% 100%;
        -webkit-transform: scale(1, 0);
        -ms-transform: scale(1, 0);
        -moz-transform: scale(1, 0);
        -o-transform: scale(1, 0);
        transform: scale(1, 0);
    }
}

/*
===============
End Down Arrow
===============
*/

@keyframes blink {
    from {
        opacity: 1;
    } to {
        opacity: 0;
    }
}

@keyframes lineGrowth {
    0% {
        transform-origin: left center;
        transform: translate3d(0,0,0) scaleX(0);
    } 50% {
        transform-origin: left center;
        transform: translate3d(0,0,0) scaleX(1);
    } 50.1% {
        transform-origin: right center;
        transform: translate3d(0,0,0) scaleX(1);
    } 100% {
        transform-origin: right center;
        transform: translate3d(0,0,0) scaleX(0);
    }
}

@keyframes handRotation {
    from {
        transform: rotate(10deg);
    } to {
        transform: rotate(50deg);
    }
}

/*
========
Opacity
========
*/
@media screen and (max-width: 1500px) {
    .page {
        &--0 {
            .wrapper {
                h1 {
                    font-size: 15rem;
                }
            }
        }
    }
}
@media screen and (max-width: 1360px) {
    .page {
        &--0 {
            .wrapper {
                h1 {
                    font-size: 18rem;
                }
            }
        }
    }
}
@media screen and (max-width: 1200px) {
    #header {
        padding: 0 150px 0 180px;
    }
    .page {
        &--0 {
            .wrapper {
                padding: 8rem 150px 0 150px;
                h1 {
                    font-size: 18rem;
                }
            }
            .scroll-icon {
                right: 150px;
            }
        }
        &--2 {
            padding: 14.5rem 10%;
            .page-container {
                max-width: 740px;
                .main-content {
                    span::after {
                        bottom: 6px;
                    }
                }
    }
            }
        }
}
@media screen and (max-width: 900px) {
    #header {
        padding: 0 120px 0 180px;
    }
    .page {
        &--0 {
            .wrapper {
                padding: 6rem 120px 0 120px;
                h1 {
                    font-size: 18rem;
                }
            }
            .scroll-icon {
                right: 120px;
            }
        }        
        &--3 {
            .footer {
                .name {
                    font-size: 3rem;
                }
            }
        }
    }
}
@media screen and (max-width: 768px) {
    .page {
        &--0 {
            .wrapper {
                h1 {
                    font-size: 13rem;
                }
                h2 {
                    font-size: 3rem;
                }
            }
        }
        &--1 {
            height: 280vh;
        }
    }
}
@media screen and (max-width: 600px) {
    #header {
        padding: 0 40px 0 0;
    }
    .page {
        &--0 {
            .wrapper {
                padding: 0 40px;
                h1 {
                    font-size: 13rem;
                }
            }
            .scroll-icon {
                right: 40px;
            }
        }
        &--1 {
            height: 180vh;
            .scrollable {
                &__banner {
                    &--inner {
                        span {
                            font-size: 13rem;
                        }
                    }
                }
            }
        }
        &--3 {
            .main {
                p {
                    font-size: 13rem;
                }
            }
            .footer {
                padding: 0 14rem 0 12rem;
            }
        }
    }
}
@media screen and (max-width: 480px) {
    .page {
        &--0 {
            .wrapper {
                h1 {
                    font-size: 10rem;
                }
            }
            .scroll-icon {
                right: 40px;
            }
        }
        &--1 {
            height: 180vh;
            .scrollable {
                &__banner {
                    &--inner {
                        span {
                            font-size: 13rem;
                        }
                    }
                }
            }
        }
        &--3 {
            .main {
                p {
                    font-size: 10rem;
                }
            }
            .footer {
                padding: 0 8rem 0 8rem;
            }
        }
    }
}
@media screen and (max-width: 320px) {
    .page {
        &--0 {
            .wrapper {
                h1 {
                    font-size: 6rem;
                }
            }
            .scroll-icon {
                right: 40px;
            }
        }
        &--1 {
            height: 200vh;
            .scrollable {
                &__banner {
                    &--inner {
                        span {
                            font-size: 10rem;
                        }
                    }
                }
            }
            .infos-container {
                max-width: none;
                min-width: 300px;
            }
        }
        &--2 {
            .page-container {
                span {
                    font: {
                        size: 2.4rem;
                    }
                }
                .main-content {
                    p, span {
                        font-size: 4.6rem;
                    }
                    span::after {
                        bottom: 4px;
                    }
                }
            }
        }
        &--3 {
            .main {
                p {
                    font-size: 6rem;
                }
            }
            .footer {
                padding: 0 10px 0 10px;
            }
        }
    }
}
</style>