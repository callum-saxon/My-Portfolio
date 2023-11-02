<template>
    <v-container class="text-details text">
      <div class="title">
        <h1>Hey, I'm <span class="highlight">Callum</span> <br> A <span class="typewrite" data-type='["Software Engineer.", "Full-Stack Developer.", "Student."]'></span>
        </h1>
        <div class="social-buttons">
          <div class="button-pair">
            <v-btn variant="plain" icon href="https://www.linkedin.com/in/callum-saxon-8072b6203/">
              <v-icon size="30">mdi-linkedin</v-icon>
            </v-btn>
            <v-btn variant="plain" icon href="https://github.com/CallumSaxon91">
              <v-icon size="30">mdi-github</v-icon>
            </v-btn>
          </div>
          <div class="button-pair">
            <v-btn variant="plain" icon href="https://stackoverflow.com/users/22798046/callum-saxon">
              <v-icon size="30">mdi-stack-overflow</v-icon>
            </v-btn>
            <v-btn variant="plain" icon @click="openGmail">
              <v-icon size="30">mdi-gmail</v-icon>
            </v-btn>
          </div>
        </div>
      </div>
    </v-container>
    <v-container class="text-details text">
      <div class="about-card">
        <div class="about-card__image-container"></div>
        <svg class="about-card__svg" viewBox="0 0 800 500">
          <defs>
            <linearGradient id="gradient" x1="0%" y1="0%" x2="100%" y2="0%">
              <stop offset="0%" style="stop-color: #d000ff"/>
              <stop offset="100%" style="stop-color: #9900ff"/>
            </linearGradient>
          </defs>
          <path
            d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650 300 Q 750 450 800 400 L 800 500 L 0 500"
            stroke="transparent" fill="#333"></path>
          <path class="about-card__line"
                d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650 300 Q 750 450 800 400"
                stroke="url(#gradient)" stroke-width="10" fill="transparent"></path>
        </svg>
        <div class="about-card__content">
          <h3 class="about-card__title">// About me</h3><br>
          <p>As a Nottingham-based full-stack developer and student, I've honed my programming skills since a young
            age
            and amassed valuable experience through diverse software projects. Driven by a unique outlook and
            analytical
            approach to software development, my passion for technology fuels my dedication to transforming complexity
            into user-friendly digital experiences. Crafting impactful solutions is my forte as a seasoned software
            engineer, thriving on turning ideas into reality. Continuously seeking opportunities for skill refinement,
            I'm eagerly open to collaborating on challenging projects.</p><br>
          <p>Some technologies I've been working with lately:</p>
          
          <div class="scroller" data-direction="right" data-speed="medium">
            <div class="scroller__inner">
              <img src="../assets/html-icon.png" height="50" width="50"/>
              <img src="../assets/vuejs-icon.png" height="50" width="50"/>
              <img src="../assets/vuetify-icon.png" height="50" width="50"/>
              <img src="../assets/axios.png" height="10" width="50" style="margin-top: 17px"/>
              <img src="../assets/javascript-icon.png" height="50" width="50"/>
              <img src="../assets/typescript-icon.png" height="50" width="50"/>
              <img src="../assets/sql-icon.png" height="50" width="50"/>
              <img src="../assets/git-icon.png" height="50" width="50"/>
              <img src="../assets/java-icon.png" height="50" width="50"/>
              <img src="../assets/c++-icon.png" height="50" width="50"/>
              <img src="../assets/python-icon.png" height="50" width="50"/>
            </div>
          </div>
        </div>
      </div>
    </v-container>
</template>

<style>
.title {
  font-size: 2rem;
  line-height: 1.4;
  text-align: left;
  padding-bottom: 20px;
}

@media (max-width: 768px) {
  .title {
    font-size: 0.85rem;
  }
}

.social-buttons {
  display: flex;
  flex-wrap: wrap;
}

.button-pair {
  display: flex;
  margin-bottom: 10px;
}

@media (max-width: 768px) {
  .button-pair {
    flex-direction: column;
    align-items: center;
  }
}

.about-card {
  position: relative;
  background: #333;
  width: 60%;
  min-height: fit-content;
  height: 100%;
  padding: 2rem;
  color: #aaa;
  border-radius: 25px;
  box-shadow: 1.5vw 1.5vw 3vw #121212, -1.5vw -1.5vw 3vw #313131;
  overflow: hidden;
  margin: 0 auto;
  font-size: large;
}

@media (max-width: 1800px) {
  .about-card {
    width: 80%;
  }
}

@media (max-width: 768px) {
  .about-card {
    width: 100%;
  }
}

.about-card__image-container {
  margin: -2rem -2rem 1rem -2rem;
}

.about-card__line,
.about-card__content {
  opacity: 0;
}

.about-card__line {
  animation: LineFadeIn .8s .5s forwards ease-in;
}

.about-card__image,
.about-card__content {
  animation: fadeAndMoveUp .8s .5s forwards;
  font-size: large;
}

.about-card__title {
  color: white;
  margin-top: 3.5vw;
  margin-bottom: 1vw;
  font-weight: 800;
  letter-spacing: 0.01em;
}

.about-card__svg {
  position: absolute;
  left: 0;
  top: 10vw;
}

@keyframes LineFadeIn {
  0% {
    opacity: 0;
    d: path("M 0 300 Q 0 300 0 300 Q 0 300 0 300 C 0 300 0 300 0 300 Q 0 300 0 300 ");
    stroke: #e1a1ff;
  }

  50% {
    opacity: 1;
    d: path("M 0 300 Q 50 300 100 300 Q 250 300 350 300 C 350 300 500 300 650 300 Q 750 300 800 300");
    stroke: url(#gradient);
  }

  100% {
    opacity: 1;
    d: path("M -2 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650 300 Q 750 450 802 400");
    stroke: url(#gradient);
  }
}

@keyframes fadeAndMoveUp {
  0% {
    transform: translateY(-1rem);
    opacity: 0;
  }

  100% {
    transform: translateY(0);
    opacity: 1;
  }
}

.highlight {
  position: relative;
  display: inline-block;
}

.highlight::after {
  content: '';
  position: absolute;
  bottom: 0;
  height: 10px;
  width: 100%;
  background: linear-gradient(to right, #d000ff, #9900ff);
  transform: skewX(-45deg);
  transform-origin: bottom left;
  right: 0;
}

@media (min-width: 768px) {
  .about-card {
    font-size: 1rem;
    border-radius: 1rem;
    float: none;
  }

  .about-card__title {
    margin-top: 1rem;
    margin-bottom: 0.5rem;
  }

  .about-card__svg {
    top: -2rem;
  }
}

.typewrite > .wrap {
  border-right: 0.08em solid transparent;
  background: linear-gradient(to right, #d000ff, #9900ff);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  padding-top: 20px;
}

.scroller {
  width: 100%;
  --_animation-duration: 40s;
}

.scroller__inner {
  padding-block: 1rem;
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
}

.scroller[data-animated="true"] {
  overflow: hidden;
  -webkit-mask: linear-gradient(
    90deg,
    transparent,
    white 20%,
    white 80%,
    transparent
  );
  mask: linear-gradient(90deg, transparent, white 20%, white 80%, transparent);
}

.scroller[data-animated="true"] .scroller__inner {
  width: max-content;
  flex-wrap: nowrap;
  animation: scroll var(--_animation-duration, 40s) var(--_animation-direction, forwards) linear infinite;
}

.scroller[data-direction="right"] {
  --_animation-direction: reverse;
}

@keyframes scroll {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-100%);
  }
}
</style>

<script lang="ts">
const TxtType = function (el, toRotate, period) {
  this.toRotate = toRotate;
  this.el = el;
  this.loopNum = 0;
  this.period = parseInt(period, 10) || 2000;
  this.txt = '';
  this.tick();
  this.isDeleting = false;
};

function startTypewriterAnimation() {
  const elements = document.getElementsByClassName('typewrite');
  for (let i = 0; i < elements.length; i++) {
    const toRotate = elements[i].getAttribute('data-type');
    const period = elements[i].getAttribute('data-period');
    if (toRotate) {
      new TxtType(elements[i], JSON.parse(toRotate), period);
    }
  }
  const css = document.createElement("style");
  css.type = "text/css";
  css.innerHTML = ".typewrite > .wrap { border-right: 0.08em solid #fff}";
  document.body.appendChild(css);
}

TxtType.prototype.tick = function () {
  const i = this.loopNum % this.toRotate.length;
  const fullTxt = this.toRotate[i];

  if (this.isDeleting) {
    this.txt = fullTxt.substring(0, this.txt.length - 1);
  } else {
    this.txt = fullTxt.substring(0, this.txt.length + 1);
  }

  this.el.innerHTML = '<span class="wrap">' + this.txt + '</span>';

  const that = this;
  let delta = 200 - Math.random() * 100;

  if (this.isDeleting) {
    delta /= 2;
  }

  if (!this.isDeleting && this.txt === fullTxt) {
    delta = this.period;
    this.isDeleting = true;
  } else if (this.isDeleting && this.txt === '') {
    this.isDeleting = false;
    this.loopNum++;
    delta = 500;
  }

  setTimeout(function () {
    that.tick();
  }, delta);
};

function startScrollerAnimation() {
  const scrollers = document.querySelectorAll(".scroller");

  if (!window.matchMedia("(prefers-reduced-motion: reduce)").matches) {
    addAnimation(scrollers);
  }

  function addAnimation(scrollers) {
    scrollers.forEach((scroller) => {
      scroller.setAttribute("data-animated", true);

      const scrollerInner = scroller.querySelector(".scroller__inner");
      const scrollerContent = Array.from(scrollerInner.children);

      scrollerContent.forEach((item) => {
        const duplicatedItem = item.cloneNode(true);
        duplicatedItem.setAttribute("aria-hidden", true);
        scrollerInner.appendChild(duplicatedItem);
      });
    });
  }
}

export default {
  mounted() {
    startTypewriterAnimation();
    startScrollerAnimation();
  },
};
</script>
