<template>
  <div>
    <TheNavigation></TheNavigation>
    <main>
      <header>
        <div class="header-banner">
          <div class="header-title">
            <h1>Mikołajkowy Hackathon</h1>
            <h2>Spraw sobie prezent na Mikołajki za 10.000 PLN!</h2>
            <div class="btn-wrapper">
              <a href="#" class="header-btn">Weź udział</a>
              <div>
                <p class="header-text">
                  Zacznij przygode z Web3 poznajac technologię smart kontraktów
                  Warp
                </p>
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
          <span>23:59 05.12.2022 ⏱️</span>
        </div>
        <div class="extra-info">
          <p>
            *Zarejestruj się wcześniej, a damy Ci feedback na temat pomysłu, co
            zdecydowanie zwiększy szanse na zwycięstwo i wyeliminuje ryzyko
            pracy nad aplikacją, która ma małe szanse na nagrodę.
          </p>
        </div>
      </section>

      <section id="prize">
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

      <section id="instruction">
        <h2>Jak wziąć udział?</h2>
        <div class="timeline">
          <div class="step">
            <p class="title">Krok 1</p>
            <p class="text">
              Poznaj Web3 & Warp SDK poprzez
              <a href="https://warp.cc" target="_blank">Warp Academy</a>
            </p>
            <span class="icon">👇</span>
          </div>

          <div class="step">
            <p class="title">Krok 2</p>
            <p class="text">
              Wymyśl kreatywny pomysł zastosowania Warp SDK i zacznij budować
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

      <section id="examples">
        <div class="accordion">
          <h2>Przykładowe projekty</h2>
          <div class="tabs">
            <div class="tab">
              <input type="checkbox" id="chck1" />
              <label class="tab-label" for="chck1">DeFi</label>
              <div class="tab-content">
                <p><span>👉</span> Zdecentralizowana giełda (DEX)</p>
                <p><span>👉</span> Zdecentralizowany protokół pożyczkowy</p>
                <p>
                  <span>👉</span> Zdecentralizowany Protokół monetyzacji danych
                </p>
              </div>
            </div>
            <div class="tab">
              <input type="checkbox" id="chck2" />
              <label class="tab-label" for="chck2">Social Apps</label>
              <div class="tab-content">
                <p>
                  <span>👉</span> Social Media - np. Instagram oparty na
                  technologii blockchain
                </p>
                <p>
                  <span>👉</span> Social Networks - Narzędzia do budowy
                  wirtualnych społeczności
                </p>
                <p>
                  <span>👉</span> Protokół Zarządzający potwierdzeniem
                  tożsamości w oparciu o technologię blockchain
                </p>
              </div>
            </div>

            <div class="tab">
              <input type="checkbox" id="chck3" />
              <label class="tab-label" for="chck3">Gaming</label>
              <div class="tab-content">
                <p>
                  <span>👉</span> Trading card games: dodaj budowanie decku,
                  wymianę kart oraz zapis wyników pojedynków na blockchainie
                </p>
                <p>
                  <span>👉</span> RPGs: tokenizacja oraz możliwość wymiany/
                  sprzedaży przedmiotów w grze
                </p>
                <p>
                  <span>👉</span> MMO: Zdefiniuj mechanizm interakcji
                  bezpośrednio w kontraktach Warp
                </p>
              </div>
            </div>
          </div>
        </div>
      </section>

      <footer></footer>
    </main>
  </div>
</template>

<script>
import TheNavigation from './components/TheNavigation.vue';

export default {
  components: {
    TheNavigation,
  },
  data() {
    return {};
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
    }

    .header-btn {
      display: flex;
      justify-content: center;
      align-items: center;
      align-self: flex-end;
      transition: all 0.3s;

      width: 70%;
      height: 5rem;

      background-color: $primary;
      border: none;
      border-radius: 1.5rem;
      color: white;
      font-size: 1.6rem;
      font-weight: bold;
      text-decoration: none;
    }

    .btn-wrapper {
      display: flex;
      flex-direction: column;
      margin-top: 2rem;
      div {
        display: flex;
        justify-content: flex-end;
      }
    }
    .header-text {
      text-align: end;
      width: 70%;
      align-self: flex-end;
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
    background-color: $secondary;

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
        font-size: 1.2rem;
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
          font-size: 1.6rem;
          color: $text-basic;
          span {
            font-size: 1.6rem;
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
          font-size: 1.4rem;

          a {
            font-size: 1.4rem;
          }
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
        background-color: $secondary;
        color: white;
        text-decoration: none;
        border-radius: 1.5rem;
        text-transform: uppercase;
        font-size: 1.4rem;
        font-weight: bold;
      }
    }
  }

  #examples {
    display: flex;
    justify-content: center;
    align-items: center;

    padding: 4rem 2rem;
    margin-top: 4rem;
    .accordion {
      h2 {
        @include section-header;
        text-align: center;
      }
      input {
        position: absolute;
        opacity: 0;
        z-index: -1;
      }
      // Layout
      .row {
        display: flex;
        .col {
          flex: 1;
          &:last-child {
            margin-left: 1em;
          }
        }
      }

      .tabs {
        margin-top: 4rem;
        border-radius: 0.8rem;
        overflow: hidden;
        box-shadow: 0 0.4rem 0.4rem -0.2rem rgba(0, 0, 0, 0.5);
      }
      .tab {
        width: 100%;
        color: white;
        overflow: hidden;
        &-label {
          display: flex;
          justify-content: space-between;
          padding: 1rem;
          background: $secondary;
          font-weight: bold;
          font-size: 2rem;
          cursor: pointer;

          &:hover {
            background: $secondary;
          }
          &::after {
            content: '\276F';
            width: 1rem;
            height: 1rem;
            text-align: center;
            transition: all 0.35s;
          }
        }
        &-content {
          max-height: 0;
          padding: 0 1em;
          background: white;
          transition: all 0.35s;

          p {
            font-size: 1.4rem;
            color: $text-basic;
            padding: 1rem 0;
            display: flex;
            align-items: center;

            span {
              font-size: 2rem;
              margin-right: 1rem;
            }
          }
        }
        &-close {
          display: flex;
          justify-content: flex-end;
          padding: 1em;
          font-size: 0.75em;
          background: $secondary;
          cursor: pointer;
          &:hover {
            background: $secondary;
          }
        }
      }

      // :checked
      input:checked {
        + .tab-label {
          background: $secondary;
          &::after {
            transform: rotate(90deg);
          }
        }
        ~ .tab-content {
          max-height: 100vh;
          padding: 1rem;
        }
      }
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

        background-color: $primary;
        border: none;
        border-radius: 1.5rem;
        color: white;
        font-size: 1.6rem;
        font-weight: bold;
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

      background-color: $secondary;
    }

    #prize {
      ul {
        display: flex;
        flex-direction: row;
        gap: 3rem;
      }
    }
  }
}

@media (min-width: 1023px) {
  main {
    header {
      padding: 0 12rem;
    }
  }
}
</style>
