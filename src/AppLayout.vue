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
              <button class="header-btn">Weź udział</button>
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
      align-self: flex-end;

      width: 70%;
      height: 5rem;

      background-color: $primary;
      border: none;
      border-radius: 1.5rem;
      color: white;
      font-size: 1.6rem;
      font-weight: bold;
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

    padding: 0 2rem;
    padding-top: 2rem;

    h2 {
      font-size: 3rem;
      color: $primary;
    }

    ul {
      list-style: none;

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
