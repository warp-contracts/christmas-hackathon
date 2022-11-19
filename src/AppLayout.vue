<template>
  <div>
    <TheNavigation @go-section="goToSection"></TheNavigation>
    <main>
      <header ref="start">
        <div class="header-banner">
          <div class="header-title">
            <h2>
              Spraw sobie prezent pod Choinkę za
              <span class="header-amount">10.000 PLN!</span>
            </h2>
            <h1>Gwiazdkowy Hackathon</h1>
            <div class="text-wrapper">
              <p class="header-text">
                Zacznij przygodę z Web3 poznając technologię smart kontraktów
                Warp
              </p>
            </div>
            <div class="btn-wrapper">
              <div class="header-buttons">
                <a href="#" class="header-btn" @click="goToSection('instruction')">Weź udział</a>
                <a href="#" class="discord-btn">Podyskutuj o pomyśle</a>
              </div>
            </div>
          </div>

          <div class="header-img">
            <img
              src="./assets/undraw_santa_visit_re_oiwr.svg"
              alt="santa picture"
            />
          </div>
        </div>
      </header>
      <section id="date">
        <div class="basic-info">
          <p>Czas zgłoszeń do:</p>
          <span>23:59 23.12.2022 ⏱️</span>
        </div>
        <div class="extra-info">
          <p>
            *Zarejestruj się wcześniej, a damy Ci feedback na temat pomysłu, co
            zdecydowanie zwiększy szanse na zwycięstwo i wyeliminuje ryzyko
            pracy nad aplikacją, która ma małe szanse na nagrodę.
          </p>
        </div>
      </section>

      <section ref="prize" id="prize">
        <h2>Nagrody</h2>
        <ul>
          <li class="first-place">
            <div>🥇</div>
            <p>Miejsce: <span class="prize-amount">10.000</span> PLN</p>
          </li>
          <li class="second-place">
            <div>🥈</div>
            <p>Miejsce: <span class="prize-amount">3.000</span> PLN</p>
          </li>
          <li class="third-place">
            <div>🥉</div>
            <p>Miejsce: <span class="prize-amount">2.000</span> PLN</p>
          </li>
        </ul>
      </section>

      <section ref="instruction" id="instruction">
        <h2>Jak wziąć udział?</h2>
        <div class="timeline">
          <div class="step">
            <p class="title">Krok 1</p>
            <p class="text">
              Poznaj Web3 & Warp SDK poprzez
              <a href="https://academy.warp.cc" target="_blank">Warp Academy</a>
            </p>
            <p class="text-extra">
              Potrzebujesz pomocy? Wbij na nasz
              <a href="https://discord.com/invite/PVxBZKFr46">Discord!</a>
            </p>
            <span class="icon">👇</span>
          </div>

          <div class="step">
            <p class="title">Krok 2</p>
            <p class="text">
              Wymyśl kreatywny pomysł zastosowania Warp SDK i zacznij budować.
            </p>
            <p class="text">
              Nie masz koncepcji na projekt? Poniej przygotowaliśmy przykładowe
              pomysły na aplikacje :)
            </p>
            <span class="icon">👇</span>
          </div>

          <div class="step">
            <p class="title">Krok 3</p>
            <p class="text">Zarejestruj swój projekt przez Google Forms</p>
            <a
              href="https://docs.google.com/forms/d/e/1FAIpQLSfD57FcJ4qOLVZ4pDYp4RNGlm99-zxVeX88bLyDF7ze0VWOSA/viewform"
              target="_blank"
              class="register-btn"
              >zarejestruj</a
            >
          </div>
        </div>
      </section>

      <section ref="examples" id="examples">
        <h2>Przykładowe projekty</h2>
        <swiper
          :modules="modules"
          :pagination="{
            clickable: true,
          }"
          class="mySwiper"
        >
          <swiper-slide>
            <h3>Social Apps</h3>
            <div class="tab-content">
              <ul>
                <li>
                  Social Media - np. Instagram oparty na technologii blockchain
                </li>
                <li>
                  Social Networks - Narzędzia do budowy wirtualnych społeczności
                </li>
                <li>
                  Protokół Zarządzający potwierdzeniem tożsamości w oparciu o
                  technologię blockchain
                </li>
              </ul>
            </div> </swiper-slide
          ><swiper-slide>
            <h3>DeFi</h3>
            <div class="tab-content">
              <ul>
                <li>Zdecentralizowana giełda (DEX)</li>
                <li>Zdecentralizowany protokół pożyczkowy</li>
                <li>Zdecentralizowany Protokół monetyzacji danych</li>
              </ul>
            </div> </swiper-slide
          ><swiper-slide>
            <h3>Gaming</h3>
            <div class="tab-content">
              <ul>
                <li>
                  Trading card games: dodaj budowanie decku, wymianę kart oraz
                  zapis wyników pojedynków na blockchainie
                </li>
                <li>
                  RPGs: tokenizacja oraz możliwość wymiany/ sprzedaży
                  przedmiotów w grze
                </li>
                <li>
                  MMO: Zdefiniuj mechanizm interakcji bezpośrednio w kontraktach
                  Warp
                </li>
              </ul>
            </div>
          </swiper-slide>
        </swiper>
      </section>

      <footer ref="contact">
        <div class="links-section">
          <a href="http://warp.cc" target="_blank">warp.cc</a>
          <a href="https://github.com/warp-contracts" target="_blank"
            ><img src="./assets/github.svg" alt="github icon link" srcset=""
          /></a>
          <a href="https://twitter.com/warp_contracts" target="_blank"
            ><img src="./assets/twitter.svg" alt="medium icon link" srcset=""
          /></a>
          <a href="https://discord.com/invite/PVxBZKFr46" target="_blank"
            ><img src="./assets/discord.svg" alt="discord icon link" srcset=""
          /></a>
        </div>
        <div class="email-section">
          <p>contest@redstone.finance</p>
          <p class="copyright">© RedStone 2022</p>
        </div>
      </footer>
    </main>
    <div class="snowflakes" aria-hidden="true">
      <div class="snowflake">❅</div>
      <div class="snowflake">❆</div>
      <div class="snowflake">❅</div>
      <div class="snowflake">❆</div>
      <div class="snowflake">❅</div>
      <div class="snowflake">❆</div>
      <div class="snowflake">❅</div>
      <div class="snowflake">❆</div>
      <div class="snowflake">❅</div>
      <div class="snowflake">❆</div>
      <div class="snowflake">❅</div>
      <div class="snowflake">❆</div>
    </div>
  </div>
</template>

<script>
import TheNavigation from './components/TheNavigation.vue';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import { Pagination } from 'swiper';

export default {
  components: {
    TheNavigation,
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      modules: [Pagination],
    };
  },

  methods: {
    goToSection(value) {
      const top = this.$refs[value].offsetTop;
      window.scrollTo({
        top: top - 90,
        left: 0,
        behavior: 'smooth',
      });
    },
  },
};
</script>

<style lang="scss" scoped>
@import './styles/variables';
@import './styles/mixins';

main {
  margin-top: 9rem;

  header {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    padding: 0 2rem;
    padding-top: 2rem;
    h1 {
      font-size: 2.6rem;
      text-align: center;
      color: $secondary;
    }
    h2 {
      font-size: 1.8rem;
      margin-top: 0.3rem;
      text-align: center;
      color: $text-basic;
      font-weight: 400;

      .header-amount {
        font-weight: bold;
        font-size: 2rem;
      }
    }

    .btn-wrapper {
      display: flex;
      flex-direction: column;
      margin-top: 2rem;

      .header-buttons {
        display: flex;
        align-items: center;
        gap: 1.5rem;

        .header-btn {
          display: flex;
          justify-content: center;
          align-items: center;
          align-self: flex-end;
          transition: all 0.3s;

          width: 47%;
          height: 5rem;

          background-color: $primary;
          border: none;
          border-radius: 50rem;
          color: white;
          font-size: 1.6rem;
          font-weight: 400;
          text-decoration: none;
        }

        .discord-btn {
          text-align: center;
          font-size: 1.6rem;
          text-decoration: none;
          color: $primary;
          font-weight: 500;
          width: 47%;
        }
      }
      .text-wrapper {
        display: flex;
        justify-content: flex-end;
      }
    }
    .header-text {
      align-self: flex-end;
      font-size: 1.8rem;
      color: $text-basic;
      margin-top: 1rem;
    }
    .header-img {
      margin-top: 1rem;
      display: flex;
      justify-content: center;
      img {
        width: 30rem;
      }
    }
  }

  #date {
    height: 25rem;
    margin-top: 4rem;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    padding: 0 2rem;
    background-color: $primary;
    box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
    div {
      color: white;
    }

    .basic-info {
      p,
      span {
        font-size: 2.6rem;
      }

      span {
        font-weight: bold;
      }
    }

    .extra-info {
      text-align: center;
      margin-top: 1rem;
      p {
        font-size: 1.4rem;
        font-style: italic;
      }
    }
  }

  #prize {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    padding: 2rem 2rem;
    margin-top: 4rem;

    h2 {
      @include section-header;
    }

    ul {
      list-style: none;
      margin-top: 2rem;

      li {
        display: flex;
        align-items: center;
        justify-content: center;
        margin-top: 1rem;
        div {
          font-size: 4rem;
        }
        p {
          margin-left: 0.5rem;
          font-size: 2.2rem;
          color: $text-basic;
          span {
            font-size: 2.2rem;
            font-weight: bold;
            color: $text-basic;
          }
        }
      }
    }
  }

  #instruction {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;

    padding: 4rem 2rem;
    margin-top: 4rem;
    background-color: $backgroundGrey;

    h2 {
      @include section-header;
    }
    .timeline,
    .step {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      margin-top: 2rem;

      .step {
        .title {
          font-size: 2rem;
          font-weight: bold;
          color: $text-basic;
        }

        .text {
          text-align: center;
          font-size: 1.6rem;

          a {
            font-size: 1.6rem;
          }
        }

        .text-extra,
        a {
          font-size: 1.6rem;
          text-align: center;
        }

        .icon {
          font-size: 3rem;
          margin-top: 2rem;
        }
      }
      .register-btn {
        margin-top: 4rem;
        display: flex;
        justify-content: center;
        align-items: center;
        width: 20rem;
        height: 5rem;
        background-color: $primary;
        color: white;
        text-decoration: none;
        border-radius: 50rem;
        text-transform: uppercase;
        font-size: 1.4rem;
      }
    }
  }

  #examples {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    height: 60rem;

    padding: 4rem 2rem;
    margin-top: 4rem;

    h2 {
      @include section-header;
      text-align: center;
    }
    .swiper {
      width: 80%;
      height: 100%;
    }

    .swiper-slide {
      text-align: center;
      font-size: 1.8rem;
      background: #fff;
      padding: 0 2.5rem;

      display: flex;
      flex-direction: column;
      -webkit-box-pack: center;
      -ms-flex-pack: center;
      -webkit-justify-content: center;
      justify-content: center;
      -webkit-box-align: center;
      -ms-flex-align: center;
      align-items: center;

      h3 {
        margin: 0 auto;
        text-align: center;
        font-size: 1.8rem;
        color: $primary;
      }

      .tab-content {
        ul {
          list-style: none;
        }
        ul li {
          text-align: left;
          font-size: 1.4rem;
          padding: 0.7rem 0;
          padding-left: 1rem;
          color: $text-basic;
        }
        ul li::marker {
          content: '👉';
          font-size: 2rem;
        }
      }
    }
  }

  footer {
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;

    margin-top: 2rem;
    padding: 0 2rem;
    background-color: $primary;
    .email-section,
    .links-section {
      gap: 1rem;
      display: flex;
      justify-content: center;
      align-items: center;
      color: white;

      p {
        font-size: 1.6rem;
      }

      a {
        color: white;
        font-size: 1.6rem;
        text-align: center;
      }
    }

    .links-section {
      margin-top: 1rem;
    }

    .email-section {
      flex-direction: column;
    }

    .copyright {
      margin: 1rem 0;
      color: white;
    }
  }
}

@media (min-width: 768px) {
  main {
    header {
      padding: 0 4rem;
      .header-banner {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;

        width: 100%;
      }
      h1 {
        font-size: 3.8rem;
        text-align: left;
      }
      h2 {
        font-size: 1.8rem;
        margin-top: 0.3rem;
        text-align: left;
      }

      .header-btn {
        align-self: flex-start;

        width: 80%;
        height: 5rem;
        cursor: pointer;
      }

      .btn-wrapper {
        margin-top: 2rem;
        justify-content: flex-start;
        div {
          justify-content: flex-start;
        }
        .header-text {
          text-align: start;
          width: auto;
        }
      }
    }

    #date {
      height: 20rem;
      padding: 0 4rem;
    }

    #prize {
      ul {
        display: flex;
        flex-direction: row;
        gap: 3rem;
      }
    }

    #examples {
      height: 50rem;
    }

    footer {
      flex-direction: row-reverse;
      justify-content: space-between;
      padding: 1rem 2rem;

      gap: 1rem;

      .links-section,
      .email-section {
        flex-direction: row;
      }

      .email-section {
        flex-direction: row-reverse;
      }
      .links-section {
        margin-top: 0;
      }

      .copyright {
        font-size: 1.2rem;
        margin: 0;
      }
    }
  }
}

@media (min-width: 1023px) {
  main {
    header {
      padding: 0 8rem;
    }

    #date {
      padding: 0 8rem;
    }

    #examples {
      padding: 0 8rem;
      height: 40rem;

      .swiper {
        width: 70%;
      }
    }

    footer {
      margin-top: 8rem;
      padding: 1rem 8rem;

    }
  }
}

@media (min-width: 1100px) {
  main {
    header {
      .header-img {
        img {
          width: 40rem;
        }
      }
    }
  }
}

.snowflake {
  color: #fff;
  font-size: 1em;
  font-family: Arial, sans-serif;
  text-shadow: 0 0 5px #000;
}

@-webkit-keyframes snowflakes-fall {
  0% {
    top: -10%;
  }
  100% {
    top: 100%;
  }
}
@-webkit-keyframes snowflakes-shake {
  0%,
  100% {
    -webkit-transform: translateX(0);
    transform: translateX(0);
  }
  50% {
    -webkit-transform: translateX(80px);
    transform: translateX(80px);
  }
}
@keyframes snowflakes-fall {
  0% {
    top: -10%;
  }
  100% {
    top: 100%;
  }
}
@keyframes snowflakes-shake {
  0%,
  100% {
    transform: translateX(0);
  }
  50% {
    transform: translateX(80px);
  }
}
.snowflake {
  position: fixed;
  top: -10%;
  z-index: 9999;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  cursor: default;
  -webkit-animation-name: snowflakes-fall, snowflakes-shake;
  -webkit-animation-duration: 10s, 3s;
  -webkit-animation-timing-function: linear, ease-in-out;
  -webkit-animation-iteration-count: infinite, infinite;
  -webkit-animation-play-state: running, running;
  animation-name: snowflakes-fall, snowflakes-shake;
  animation-duration: 10s, 3s;
  animation-timing-function: linear, ease-in-out;
  animation-iteration-count: infinite, infinite;
  animation-play-state: running, running;
}
.snowflake:nth-of-type(0) {
  left: 1%;
  -webkit-animation-delay: 0s, 0s;
  animation-delay: 0s, 0s;
}
.snowflake:nth-of-type(1) {
  left: 10%;
  -webkit-animation-delay: 1s, 1s;
  animation-delay: 1s, 1s;
}
.snowflake:nth-of-type(2) {
  left: 20%;
  -webkit-animation-delay: 6s, 0.5s;
  animation-delay: 6s, 0.5s;
}
.snowflake:nth-of-type(3) {
  left: 30%;
  -webkit-animation-delay: 4s, 2s;
  animation-delay: 4s, 2s;
}
.snowflake:nth-of-type(4) {
  left: 40%;
  -webkit-animation-delay: 2s, 2s;
  animation-delay: 2s, 2s;
}
.snowflake:nth-of-type(5) {
  left: 50%;
  -webkit-animation-delay: 8s, 3s;
  animation-delay: 8s, 3s;
}
.snowflake:nth-of-type(6) {
  left: 60%;
  -webkit-animation-delay: 6s, 2s;
  animation-delay: 6s, 2s;
}
.snowflake:nth-of-type(7) {
  left: 70%;
  -webkit-animation-delay: 2.5s, 1s;
  animation-delay: 2.5s, 1s;
}
.snowflake:nth-of-type(8) {
  left: 80%;
  -webkit-animation-delay: 1s, 0s;
  animation-delay: 1s, 0s;
}
.snowflake:nth-of-type(9) {
  left: 90%;
  -webkit-animation-delay: 3s, 1.5s;
  animation-delay: 3s, 1.5s;
}
.snowflake:nth-of-type(10) {
  left: 25%;
  -webkit-animation-delay: 2s, 0s;
  animation-delay: 2s, 0s;
}
.snowflake:nth-of-type(11) {
  left: 65%;
  -webkit-animation-delay: 4s, 2.5s;
  animation-delay: 4s, 2.5s;
}
</style>
